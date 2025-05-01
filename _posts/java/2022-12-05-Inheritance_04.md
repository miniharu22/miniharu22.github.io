---
title : "JAVA - 추상 클래스"
layout: single
excerpt: "[JAVA] 상속 (Inheritance) 이론 정리 - 4"
toc: true
toc_sticky: true
date: 2022-12-05
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
[상속 (Inheritance) 이론 정리 - 3](https://sun0te.github.io/java/Inheritance_03/)  

---

# Chapter 07. 상속 - 4

## 8. 추상 클래스 (Abstract Class)  

### 8.1 추상 클래스의 개념  

추상 (abstract) : 실체들 간의 공통되는 특성을 추출한 것이다.  
*ex) 강아지, 고양이, 새 → 동물 (추상)*  

**실체 클래스** : 객체를 직접 생성해 사용할 수 있는 클래스  
**추상 클래스** : 실체 클래스들의 공통적인 특성(필드, 메소드)를 추출해서 정의한 클래스  
{: .notice--info}

**상속 관계**  
추상 클래스는 단독으로 객체 생성이 불가하고, 부모 클래스로만 사용 가능하다.  
*(개념적인 부분이며 새로운 실체 클래스를 만들기 위해서 생성하기 때문이다.)*  

- **부모 : 추상 클래스**  
```java
Animal animal = new Animal();   // (X) new 연산자로 인스턴스 생성 불가
class Ant extends Animal {...}  // (O)
```
- **자식 : 실체 클래스**  
    *부모인 추상 클래스의 모든 특성을 물려받고, 추가적인 특성(필드, 메소드)을 가질 수 있다.*

  **ex)**  
  추상 클래스 `Animal.class`  
    ↑ (상속)   
  실체 클래스 `Dog.class`, `Cat.class`, `Bird.class`  

### 8.2 추상 클래스의 용도  

실체 클래스들의 공통적인 특성(필드, 메소드)을 뽑아내어 추상 클래스로 만드는 이유  

**1. 실체 클래스들의 공통된 필드와 메소드의 이름을 통일할 목적**  
- 실체 클래스를 설계하는 사람이 여러 사람일 경우  
- 실체 클래스마다 필드와 메소드가 재각기 다른 이름을 가질 수 없다.  

**2. 실체 클래스를 작성할 때 시간을 절약**  
- 실체 클래스는 추가적인 필드와 메소드만 선언하면 된다.  
- 추상 클래스의 설계 규격대로 실체 클래스를 작성하면 된다.  

### 8.3 추상 클래스 선언  
추상 클래스를 선언할 때 클래스 선언에 abstract 키워드를 붙여야 한다.  
```java
public abstract class 클래스 {
  //필드 //생성자 //메소드
}
```  
일반 클래스와 마친가지로 필드, 생성자, 메소드 선언이 가능하다. 
*(new 연산자로 직접 생성자 호출 불가)*  
자식 객체가 생성될 때 super(...) 를 호출해서 추상 클래스의 객체를 생성하므로,  
추상 클래스에도 생성자가 있어야 한다.  

- `Phone.java` 추상 클래스  
  ```java
  public abstract class Phone {
  //필드
  public String owner;
  
  //생성자
  public Phone(String owner) {
    this.owner = owner;
  }
  
  //메소드
  public void turnOn() {
    System.out.println("폰 전원을 켭니다. ");
  }
  public void turnOff() {
    System.out.println("폰 전원을 끕니다. ");
  }
  }
  ```  
- `SmartPhone.java` 실체 클래스
  ```java
  public class SmartPhone extends Phone{
  //생성자
  public SmartPhone(String owner) {
    super(owner); //Phone 의 생성자 호출
  }
  
  //메소드
  public void internetSearch() {
    System.out.println("인터넷 검색을 합니다. ");
  }
  }
  ```
- `PhoneExample.java` 자식 클래스 객체 생성, 추상 클래스 메소드 사용
  ```java
  public static void main(String[] args) {
    //Phone phone = new Phone();  //Phone 생성자 호출하여 객체 생성 불가능
    
    SmartPhone smartPhone = new SmartPhone("홍길동");
    
    smartPhone.turnOn();  //Phone의 메소드
    smartPhone.internetSearch();
    smartPhone.turnOff();  //Phone의 메소드
  }
  ```
- 
|실행 결과|
|:-----|
|폰 전원을 켭니다. <br>인터넷 검색을 합니다. <br>폰 전원을 끕니다. |

### 8.4 추상 메소드와 오버라이딩  
추상 클래스는 추상 메소드 선언이 가능하다. *(추상 클래스에서만 가능)*   
자식 클래스는 반드시 추상 메소드를 **재정의 (오버라이딩)** 해서 실행 내용을 작성해야 한다.  
아래의 예시는 추상 메소드를 선언하는 방법이다.  
```java
[public | protected] abstract 리턴타입 메소드명(매개변수, ...);
```

**일반 메소드 선언과 차이점**  
\- abstract 키워드가 붙어있다.  
\- 메소드 중괄호 {} 가 없다.  
{: .notice--info}

- `Animal.java` 추상 메소드 선언
  ```java
  public abstract class Animal {
    public String kind;

    public void breathe() {
      System.out.println("숨을 쉽니다. ");
    }
    
    public abstract void sound(); //추상 메소드
  }
  ```
- `Dog.java` 추상 메소드 오버라이딩
  ```java
  public class Dog extends Animal {
  public Dog() {
    this.kind = "포유류";
  }
  
  //추상 메소드 재정의
  @Override
  public void sound() {
    System.out.println("멍멍"); 
  }
  }
  ```
- `Cat.java` 추상 메소드 오버라이딩

  ```java
  public class Cat extends Animal {
  public Cat() {
    this.kind = "포유류";
  }
  
  //추상 메소드 재정의
  @Override
  public void sound() {
    System.out.println("야옹"); 
  }
  }
  ```
- `AnimalExample.java` 실행 클래스
  ```java
  public static void main(String[] args) {
    Dog dog = new Dog();
    Cat cat = new Cat();
    dog.sound();
    cat.sound();
    System.out.println("---------");

    //변수의 자동 타입 변환
    Animal animal = null;
    animal = new Dog();  //자동 타입 변환
    animal.sound();   //재정의된 메소드 호출
    
    animal = new Cat();  //자동 타입 변환
    animal.sound();   //재정의된 메소드 호출
    System.out.println("---------");
    
    //메소드의 다형성
    animalSound(new Dog());
    animalSound(new Cat());
  }
  
  public static void animalSound(Animal animal) { //Animal animal : 자동 타입 변환 
    animal.sound();
  }
  ```
- 
|실행 결과|
|:-----|
|멍멍<br>야옹<br>---------<br>멍멍<br>야옹<br>---------<br>멍멍<br>야옹|


🌞 정보 : 공부 기록용 블로그입니다. 오타나 내용 오류가 있을 경우 알려주시면 감사하겠습니다.
{: .notice}
