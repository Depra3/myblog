---
title: JAVA - 생성자
date: 2023/08/02 20:00:00
categories:
- JAVA
tags:
- 개념
- 객체 지향 프로그래밍
- 생성자
- 생성자 오버로딩
- 기본 생성자
- Error
---
<h1>
<details>
<summary>목차</summary>
<div markdown="1">

- [생성자](#생성자)
    - [특징](#특징)
- [기본 생성자와 매개 변수가 있는 생성자](#기본-생성자와-매개-변수가-있는-생성자)
- [주의 사항](#주의-사항)
</div>
</details>
</h1>
---

# 생성자

- **객체가 생성될 때 자동으로 호출**되어 **인스턴스 변수를 지정한 값으로 초기화하는 메소드
즉, 인스턴스 초기화 메소드이다.**

# 특징

- **생성자의 이름은 클래스의 이름과 동일**해야 한다.
- **클래스 내에서 선언**되며 **리턴 값이 없고 상속되지 않는다.**
    - **리턴 값이 없다고 반환 타입 void를 선언하지 않는다.**
- **하나의 클래스가 여러개의 생성자를 가질 수 있다.**
    - **생성자도 메소드이므로 메소드 오버로딩이 가능**
    

---

## 기본 생성자와 매개 변수가 있는 생성자

- **하나의 클래스에는 반드시 하나 이상의 생성자가 존재**해야 한다.
    - **코드 작성자가 생성자를 구현하지 않을 경우**에는 **컴파일러가 자동으로 생성자 코드를 넣는다.**
- **생성자 오버로딩이 가능하여 여러 개의 생성자를 사용할 수 있다.**
#
- **예시**
    
    ```java
    접근제어자 class 클래스명 {
    	자료형(String, int, ...) 변수명;
    
    	// 기본 생성자 - 생략 가능
    	접근제어자 클래스명() { } 
    	// 매개 변수가 있는 생성자 - 생략 불가능
    	접근제어자 클래스명(자료형 매개변수①, 자료형 매개변수②, ...) {
    		~~~
    		~~~
    	}
    
    	접근제어자 리턴타입(String, int, ...) 메소드명(){	}	
    }
    ```
    
    - **접근제어자 : [Depra3's JAVA - 접근제어자](https://depra3.github.io/2023/08/07/2023/08/JAVA-%EC%A0%91%EA%B7%BC%EC%A0%9C%EC%96%B4%EC%9E%90/)**
#
- **코드**
    
    ```java
    public class Car {
    	String model;
    	int speed;
    
    	// 필드를 직접적으로 초기화할 수도 있다.
    	String color = "빨강";
    
    	// 기본 생성자
    	public Car() { 
    		// 생략 가능. 만들어놓지 않아도 기본은 존재.
    	}
    
    	// 생성자 오버로딩
    	public Car(String model){ // 매개변수가 하나인 생성자
    		this.model = model;  // 입력받은 매개변수 값을 객체 변수에 입력
    	}
    	// 생성자 오버로딩
    	public Car(String model, int speed){ // 매개 변수가 2개인 생성자
    		this.model = model;
    		this.speed = speed;
    		this.color = color;
    	}
    
    	public void carInfo() { // 출력
    		System.out.println("제조사 : " + model + ", 속도 : " + speed);
    	}
    	public void carColor() {
    		System.out.println("자동차 색상 : " + color);
    	}
    }
    
    ----------------------------------------
    
    public class test {
    	public static void main(String[] args) {
    		Car car1 = new Car();           // 객체 생성 - 기본 생성자
    		Car car2 = new Car("BMW");      // 객체 생성 - 매개 변수 1개인 생성자
    		Car car3 = new Car("BMW", 120); // 객체 생성 - 매개 변수 2개인 생성자
    
    		car1.carInfo(); // 기본 생성자
    		car2.carInfo(); // 매개 변수 1개인 생성자
    		car3.carInfo(); // 매개 변수 2개인 생성자
    		car3.carColor();
    	}
    }
    ```
#    
- **실행 결과**
    
    ![](/Images/2023/08/JAVA-생성자/Untitled.png)
    
---

# 주의 사항

> **기본 생성자는 생략할 수 있다.** 그러나 **기본 생성자를 정의하지 않고 다른 생성자 정의가 1개 이상이 존재하는 상태**에서 **기본 생성자 호출하면 다음과 같은 Error가 발생**한다.
>   
#    
- **코드**
    
    ```java
    public class Car {
    	String model;
    	int speed;
    
    	// 필드를 직접적으로 초기화할 수도 있다.
    	String color = "빨강";
    
    	// 기본 생성자
    //	public Car() { 
    //		// 생략 가능. 만들어놓지 않아도 기본은 존재
    //	}
    
    	// 생성자 오버로딩
    	public Car(String model){ // 매개변수가 하나인 생성자
    		this.model = model;  // 입력받은 매개변수 값을 객체 변수에 입력
    	}
    	// 생성자 오버로딩
    	public Car(String model, int speed){ // 매개 변수가 2개인 생성자
    		this.model = model;
    		this.speed = speed;
    		this.color = color;
    	}
    
    	public void carInfo() { // 출력
    		System.out.println("제조사 : " + model + ", 속도 : " + speed);
    	}
    	public void carColor() {
    		System.out.println("자동차 색상 : " + color);
    	}
    }
    
    ----------------------------------------
    
    public class test {
    	public static void main(String[] args) {
    		Car car1 = new Car();           // 객체 생성 - 기본 생성자 ★ Error 발생 ★
    		Car car2 = new Car("BMW");      // 객체 생성 - 매개 변수 1개인 생성자
    		Car car3 = new Car("BMW", 120); // 객체 생성 - 매개 변수 2개인 생성자
    
    		car1.carInfo(); // 기본 생성자
    		car2.carInfo(); // 매개 변수 1개인 생성자
    		car3.carInfo(); // 매개 변수 2개인 생성자
    		car3.carColor();
    	}
    }
    ```
#    
- **실행 결과**

    ![](/Images/2023/08/JAVA-생성자/Untitled%201.png)