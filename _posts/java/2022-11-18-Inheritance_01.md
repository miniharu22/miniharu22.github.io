---
title : "JAVA - 상속, 클래스 상속, 부모 생성자 호출(super), 메소드 오버라이드(Override)"
layout: single
excerpt: "[JAVA] 상속 (Inheritance) 이론 정리 - 1"
toc: true
toc_sticky: true
date: 2022-11-18
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

# Chapter 07. 상속 - 1

## 1. 상속 (Inheritance) 개념  

부모가 자식에게 물려주는 행위로 자식은 상속을 통해 부모가 물려준 것을 사용할 수 있다.  
부모 클래스의 멤버를 자식 클래스에게 물려줄 수 있고, 이미 개발된 클래스를 재사용해서 새로운 클래스를 만들기 때문에 코드의 중복을 줄여준다.

부모 클래스의 수정으로 모든 자식 클래스들의 수정 효과를 가져오기 때문에
클래스의 수정을 최소화시키고, 유지 보수 시간을 최소화 시킨다.

\- **부모 클래스** : 상위 클래스  
\- **자식 클래스** : 하위 클래스, 또는 파생 클래스
{: .notice--info}

- `A,java` 부모 클래스
    ```java
    public class A {
        int field1;
        void method1() {...}
    }
    ```

- `B.java` 자식 클래스
    ```java
    //extends A : A를 상속
    public class 8 extends A {  
        String field2;
        void method() {...}
    }
    ```

> 실제로 B 클래스를 객체 생성해서 다음과 같이 사용할 때,   
A 클래스처럼 field1 과 method1() 을 가지고 있는 것처럼 보인다.  
```java
//A로부터 물려받은 필드와 메소드
B b = new B();
b.field1 = 10;
b.method1();
//B가 추가한 필드와 메소드
b.field2 = "김자바";
b.method2();
```
  
**상속에서 제외되는 대상**  
\- 부모 클래스에서 private 접근 제한을 갖는 필드와 메소드  
\- 부모 클래스와 자식 클래스가 다른 패키지에 존재할 시 default 접근 제한을 갖는 필드와 메소드  

## 2. 클래스 상속  

`자식 클래스 선언`

```java
class 자식 클래스 extends 부모 클래스 { 
    //필드
    //생성자
    //메소드
}
```

자바는 다중 상속을 허용하지 않는다.  
즉, 여러 개의 부모 클래스를 상속할 수 없기 때문에 extends 뒤에는 단 하나의 부모 클래스만 와야 한다.  

## 3. 부모 생성자 호출  

자식 객체를 생성하면, 부모 객체가 먼저 생성되고 자식 객체가 그 다음에 생성된다.  

```java
DmbCellPhone dmbCellPhone = new DmbCellPhone();
```

DmbCellPhone 객체만 생성하는 것처럼 보인다.  
하지만 부모인 CellPhone 객체가 먼저 생성된 후, DmbCellPhone 객체가 생성된다.
아래의 사진은 이를 메모리로 표현한 것이다.
<center><img src="/images/2022-11-18-java_Inheritance/Inheritance_memory.png"></center>

<br>
모든 객체는 클래스의 생성자를 호출해야만 생성된다.  
부모 객체를 생성하기 위해 부모 생성자는 자식 생성자의 맨 첫 줄에서 호출된다.  

- ex) `DmbCellPhone` 의 생성자가 명시적으로 선언되지 않았을 시 컴파일러가 기본 생성자를 생성  
    ```java
    public DmbCellPhone(); {
        super();    //추가됨, 부모의 기본 생성자 호출
    }
    ```

- 즉 `CellPhone` 클래스의 다음 생성자를 호출한다.  
    ```java
    public CellPhone() {
    }
    ```

- 만약 자식 생성자를 선언하고 명시적으로 부모 생성자를 호출할 시에는 다음과 같이 작성한다.
    ```java
    자식 클래스( 매개변수선언, ...) {
        super( 매개값, ... );
        ...
    }
    ```

super(매개값, ...) 는 매개값의 타입과 일치하는 부모 생성자를 호출한다.  
또한 생략될 시 자동적으로 컴파일러에 의해 추가되기 때문에 부모 생성자가 존재해야 한다.  
> **Why?**  
일치하는 부모생성자가 없을 경우 컴파일 오류가 발생한다.

부모 클래스에 기본 생성자가 없고 매개 변수가 있는 생성자만 있다면 자식 생성자에서 반드시 부모 생성자 호출을 위해 super(매개값, ...) 를 명시적으로 호출해야 한다.  
**반드시 super(매개값, ...) 는 자식 생성자 첫 줄에 위치해야 한다.**  

## 4. 메소드 재정의

어떤 메소드는 자식 클래스가 사용하기에는 부적합할 수 있다.  
이런 경우 상속된 일부 메소드를 자식 클래스에서 다시 수정하여 사용할 경우에   
자바는 **메소드 오버라이딩 (Overriding) 기능을 제공**한다.

### 4.1 메소드 재정의(@Override)  

- 메소드 오버라이딩 : 상속된 메소드의 내용이 자식 클래스에 맞지 않을 경우, 자식 클래스에서 동일한 메소드를 재정의하는 것  

메소드가 오버라이딩되었을 시 부모 객체의 메소드는 숨겨지고, 자식 객체에서 메소드를 호출하면 오버라이딩된 자식 메소드가 호출된다.
<center><img src="/images/2022-11-18-java_Inheritance/method_override.png"></center>  
<br>
<br>

**<i class="fa fa-exclamation-triangle" aria-hidden="true"></i>  메소드 오버라이딩할 때 주의할 사항**   
    - 부모의 메소드와 동일한 시그너처(리턴 타입, 메소드 이름, 매개 변수 리스트) 를 가져야 한다.  
    - 접근 제한을 더 강하게 오버라이딩 할 수 없다.  
    - 새로운 예외(Exception) 를 throws 할 수 없다. (예외는 Chapter 10에 기술)
{: .notice--info}

부모 메소드가 public 접근 제한을 가지고 있을 경우 오버라이딩하는 자식 메소드는 default 나 private 접근 제한으로 수정할 수 없기 때문에 접근 제한을 더 강하게 오버라이딩 할 수 없다.  
단, 반대로 부모 메소드가 default 접근 제한을 가지면 재정의되는 자식 메소드는 default 또는 public 접근 제한을 가질 수 있다.  

### 4.2 부모 메소드 호출(super)  

메소드 오버라이딩 시에, 부모 클래스의 메소드는 숨겨지고 오버라이딩된 자식 메소드만 사용된다.  
만일 자식 클래스 내부에서 오버라이딩 된 부모 클래스의 메소드를 호출해야 한다면 명시적으로 super 키워드를 붙여서 부모 메소드를 호출할 수 있다.  

```java
super.부모메소드();
```  

<center><img src="/images/2022-11-18-java_Inheritance/super_method.png"></center>  

🌞 정보 : 공부 기록용 블로그입니다. 오타나 내용 오류가 있을 경우 알려주시면 감사하겠습니다.
{: .notice}
