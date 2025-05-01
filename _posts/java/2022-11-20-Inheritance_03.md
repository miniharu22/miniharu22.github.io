---
title : "JAVA - 다형성, 타입 변환, Promotion, 배열 객체 관리,  Casting, Instanceof"
layout: single
excerpt: "[JAVA] 상속 (Inheritance) 이론 정리 - 3"
toc: true
toc_sticky: true
date: 2022-11-20
categories: [Java]
tag: [이것이 자바다, Inheritance]
author_profile: false
header:
  overlay_image: assets/images/header_post_1.jpg
  overlay_filter: 0.5 
  teaser: assets/images/java.png
published: true
---

*<i class="fa fa-info-circle" aria-hidden="true"></i> 이것이 자바다 의 Chapter07 을 참고하여 정리한 포스트입니다.*  

> 이전글
: [상속 (Inheritance) 이론 정리 - 1](https://sun0te.github.io/java/Inheritance_01/)  
[상속 (Inheritance) 이론 정리 - 2](https://sun0te.github.io/java/Inheritance_02/)  

---

# Chapter 07. 상속 - 3

## 7. 타입 변환과 다형성  

- 다형성 (polymorphism) : 같은 타입이지만 실행 결과가 다양한 객체를 이용할 수 있는 성질  
- 다형성 코드 측면 : 하나의 타입에 여러 객체를 대입함으로써 다양한 기능을 이용

JAVA는 다형성을 위해 부모 클래스로 타입 변환을 허용한다.  
즉, 부모 타입에 모든 자식 객체가 대입될 수 있다.  이것을 이용하면 객체는 부품화가 가능하다.  

```java
public class Car {
  // Tire : 타이어 타입 필드
  Tire t1 = new HankookTire();  //new HankookTire(); : 자식 타입 객체 대입
  Tire t2 = new KumhoTire();    //new KumhoTire(); : 자식 타입 객체 대입

  //HankookTire와 KumhoTire는 Tire를 상속했기 때문에 Tire 변수에 대입 가능
}
```

- 타입 변환 : 데이터 타입을 다른 데이터 타입으로 변환하는 행위  
- 클래스 타입 변환 : 상속 관계에 있는 클래스 사이에서 발생  

<br>

### 7.1 자동 타입 변환 (Promotion)  
프로그램 실행 도중에 자동적으로 타입 변환이 일어나는 것으로  
자식은 부모의 특징과 기능을 상속받기 때문에 부모와 동일하게 취급될 수 있다.  
 
<center><img src="/images/2022-11-18-java_Inheritance/promotion_formula.png"></center>
{: .notice--info}

> **ex)** Animal 과 Dog 클래스 상속관계
```java
class Animal{
  ...
}
```   
```java
class Dog extends Animal {
  ...
}
```
  Dog 클래스로부터 Dog 객체를 생성하고 이것을 Animal 변수에 대입하면 자동타입 변환이 일어난다.  
  ```java
  Dog dog = new Dog();ㅤ// ┐   
  Animal animal = dog;ㅤ// ┘ Animal animal = new Dog(); 도 가능  
  ```
  <center><img src="/images/2022-11-18-java_Inheritance/promotion_memory.png"></center>
  > dog 와 animal 변수는 타입만 다를 뿐, 동일한 Dog 객체를 참조한다.
  ```java
  dog == animal   //ture
  ```

---

위의 부모가 아니더라고 상속 계층에서 상위 타입이라면 자동 타입변환이 일어날 수 있다.  
![promotion_example](\images\2022-11-18-java_Inheritance\promotion_example.png)  
- D 객체는 B와 A 타입으로 자동 타입 변환 가능, C, E 타입으로는 불가능 (상속 관계 아님)  
- E 객체틑 C와 A 타입으로 자동 타입 변환 가능, B, D 타입으로는 불가능 (상속 관계 아님)  
부모 타입으로 자동 타입 변환된 이후에는 부모 클래스에 선언된 필드와 메소드만 접근이 가능하다.  
변수는 자식 객체를 참조하지만 변수로 접근 가능한 멤버는 부모 클래스 멤버로만 한정된다.  

> **<i class="fa fa-info-circle" aria-hidden="true"></i>  예외**   
메소드가 자식 클래스에서 오버라이딩 되었다면 자식 클래스의 메소드가 대신 호출된다.  
아래 예시를 보면 타입 변환 이후에도 오버라이딩된 자식 메소드가 호출된 것을 확인할 수 있다.
<br>   
![promotion_metnod](\images\2022-11-18-java_Inheritance\promotion_method.png)  
Parent 타입으로 변환된 후에는 method3()을 호출할 수 없다. *(변환 전 Child 타입은 가능)*

<br>

### 7.2 필드의 다형성  
- 자동 타입 변환이 필요한 이유 : 다형성을 구현하는 기술적 방법이기 때문이다.  
- `필드의 다형성` : 필드의 타입은 변함이 없지만, 실행 도중에 어떤 객체를 필드로 저장하느냐에 따라 실행 결과가 달라질 수 있다.  
*(필드의 값을 다양화함으로써 실행 결과가 다르게 나오도록 구현)*  

> **<i class="fa fa-question-circle"></i> 상속과 오버라이딩, 타입 변환을 이용하여 성능이 좋은 객체로 교체할 수 있는 이유**  
\- 자식 클래스는 부모가 가지고 있는 필드와 메소드를 가지고 있으니 사용 방법이 동일하다.  
\- 자식 클래스는 부모의 메소드를 오버라이딩(재정의)해서 더 좋은 실행 결과가 나오게 할 수 있으며, 또한 자식 타입을 부모 타입으로 변환할 수 있다.  

- **ex)** 필드의 다형성 코드
```java
class Car {
  //4개의 필드
  Tire frontLeftTire = new Tire();
  Tire frontRightTire = new Tire();
  Tire backLeftTire = new Tire();
  Tire backRightTire = new Tire();
  //메소드 
  void run() {...}
}
```  
```java
Car myCar = new Car();
//객체 교체
myCar.frontRightTire = new HankookTire();
myCar.backLeftTire = new KumhoTire();
myCar.run();
```
- **자식 타입이 부모 타입으로 자동 타입 변환**  
Car 객체는 Tire 클래스에 선언된 필드와 메소드만 사용하므로  
Tire 클래스 타입인 frontRightTire, backLeftTire는 <u>Tire의 자식 객체가 저장 가능하다.</u>   
(원래는 Tire 객체가 저장되어야 한다.)  
```java
void run() {
  frontLeftTire.roll();
  frontRightTire.roll();  // HankookTire roll() 메소드 호출
  backLeftTire.roll();  // KumhoTire roll() 메소드 호출
  backRightTire.roll();
}
```
- HankookTire, KumhoTire는 부모인 Tire의 필드와 메소드를 보유하고 있다.  
Car의 roll() 메소드 수정 없이 다양한 roll() 메소드의 실행 결과가 출력된다.  
<center><img src="/images/2022-11-18-java_Inheritance/fieldpolymorphism.png"></center>  

<br>

### 7.3 하나의 배열로 객체 관리  
동일한 타입의 값들은 배열로 관리하는 것이 유리하듯이 동일한 객체들도 배열로 관리할 수 있다.  

- Tire 를 부품으로 가지는 `클래스 필드`를 **배열로 수정**
```java
class Car {
  Tire frontLeftTire = new Tire("앞왼쪽", 6);
  Tire frontRightTire = new Tire("앞오른쪽", 2);
  Tire backleftTire = new Tire("뒤왼쪽", 3);
  Tire backRightTire = new Tire("뒤오른쪽", 4);
}
//------------------------------------------------
// 배열로 관리
class Car {
  Tire[] tires = {
    new Tire("앞왼쪽", 6), 
    new Tire("앞오른쪽", 2), 
    new Tire("뒤왼쪽", 3), 
    new Tire("뒤오른쪽", 4)
  };
}
```
> 인덱스 1을 이용하여 앞오른쪽 타이어를 KumhoTire 로 교체할 수 있다.  
```java
tires[1] = new KumboTire("앞오른쪽", 13);
```

- 배열로 수정된 필드를 사용한 `Car 클래스의 메소드`  
  ```java
  int run() {
    System.out.println("자동차가 달립니다. ");
    for(int i = 0; i < tires.length; i++) {
      if(tires[i].roll() == false) {
        stop();
        return (i+1);
      }
    }
    return 0;
  }

  void stop() {
    System.out.println("자동차가 멈춥니다. ");
  }
  ```

- Car `실행 클래스`
```java
public class CarExample {
public static void main(String[] args) {
  //Car 객체 생성
  Car car = new Car();
  //Car 객체의 run() 메소드 5번 반복 실행
  for(int i = 1; i <= 5; i++) {
    int problemLotation = car.run();

    if(problemLotation != 0) {
      System.out.println(car.tires[problemLotation-1].location + " HnakookTire 교체");
      car.tires[problemLotation-1] = new HankookTire(car.tires[problemLotation-1].location, 15);
    }

    System.out.println("------------------------------------------");

  }
}
}
```

<br>

### 7.4 매개 변수의 다형성  
`매개 변수의 다형성` : 매개값으로 어떤 자식 객체가 제공되느냐에 따라 메소드의 실행 결과가 다양해진다.  
(매개값의 자동 타입 변환과 메소드 오버라이딩을 이용)  

메소드를 호출할 때 매개값을 다양화하기 위해 매개 변수에 자식 타입 객체를 지정할 수 있다.  
(매개 변수의 타입과 동일한 매개값을 지정하는 것이 정석)  

**ex)** `Driver 클래스`에 정의되어 있는 drive() 메소드에 <u>Vehicle 타입의 매개 변수 선언</u>
```java
class Driver {
  void drive(Vehicle vehicle) {
    vehicle.run();
  }
}
```
- 정상적으로 `drive 메소드 호출`
```java
Driver driver = new Driver();
Vehicle vehicle = new Vehicle();
driver.drive(vehicle);
```
- drive() 메소드 호출 시 Vehicle 의 자식 클래스인 `Bus 객체`를 매개값으로 지정
```java
Driver driver = new Driver();
Bus bus = new Bus();
driver.drive( bus );  //자동 타입 변환 발생 
```  

  <img src="/images/2022-11-18-java_Inheritance/vehicle_exam.png">
  {: .notice--info}

- 매개 변수 타입이 클래스인 경우, 해당 클래스의 객체 뿐만 아니라 자식 객체까지도 매개값으로 사용할 수 있다.
```java
void drive(Vehicle vehicle) { //Vehicle ← 자식 객체
  vehicle.run();  //자식 객체가 재정의한 run() 메소드 실행
}
```  

<br>

### 7.5 강제 타입 변환 (Casting)  
강제 타입 변환 : 부모 타입을 자식 타입으로 변환하는 것으로,  
자식이 부모 타입으로 자동 변환한 후, 다시 자식 타입으로 변환할 때 사용이 가능하다.    

<center><img src="/images/2022-11-18-java_Inheritance/casting_formula.png"></center>
{: .notice--info}

> **<i class="fa fa-exclamation-triangle" aria-hidden="true"></i> 제약사항**  
자식 타입이 부모 타입으로 자동변환 후, 부모 타입에 선언된 필드와 메소드만 사용가능하다.  
만약 자식 타입에 선언된 필드와 메소드를 사용해야 한다면 강제 타입 변환으로 다시 자식 타입으로 변환한 다음 자식 타입의 필드와 메소드를 사용하면 된다.  

**ex)** field2 필드, method3() 메소드는 Child 타입에만 선언되었기 때문에 Parent 타입으로 자동 타입 변환 시 사용 불가능  
*(사용해야 한다면 Child 타입으로 다시 강제 타입 변환)*  
<center><img src="/images/2022-11-18-java_Inheritance/casting.png"></center>

<br>

### 7.6 객체 타입 확인 (instanceof)  
강제 타입 변환 : 자식 타입이 부모 타입으로 변환되어 있는 상태에서만 가능  
부모 타입의 변수가 부모 객체를 참조할 경우 자식 타입으로 변환할 수 없다.   
```java
Parent parent = new Parent();
Child child = (Child) parent; //강제 타입 변환 불가능
```

메소드 내 강제 타입 변환이 필요한 경우 반드시 매개값이 어떤 객체인지 instanceof 연산자로 확인한다.  
부모 변수가 참조하는 객체가 부모 객체인지 자식 객체인지 확인할 수 있다. 

**instanceof 연산자**  
 boolean result = *좌항*(객체) instanceof *우항*(타입)
{: .notice--info}

- **ex)** Parent 매개 변수가 참조하는 객체가 Child 인지 조사
```java
public void method (Parent parent)  {
  if(parent instanceof Child) {
    Child child = (Child) parent;
  }
}
```

🌞 정보 : 공부 기록용 블로그입니다. 오타나 내용 오류가 있을 경우 알려주시면 감사하겠습니다.
{: .notice}
