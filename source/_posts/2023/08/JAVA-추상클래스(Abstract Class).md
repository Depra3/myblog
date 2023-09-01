---
title: JAVA - 추상클래스 (Abstract Class)
date: 2023/08/26 20:30:00
categories:
- JAVA
tags:
- 개념
- 객체 지향 프로그래밍
- 패키지
- 추상 클래스
- 추상 메소드
- 미완성 설계도
- 오버라이딩
---

# **추상 클래스 (Abstract Class)**

> **하나 이상의 추상 메소드를 포함하는 클래스
추상 메소드를 선언하고, 자식 클래스에서 메소드를 완성하도록 하는 클래스**다.
따라서, **미완성 설계도**라고도 불린다.
> 

# 특징

- 객체 지향 프로그래밍에서 **중요한 특징인 다형성을 가지는 메소드의 집합을 정의**할 수 있도록 한다.
- 반드시 **사용되어야 하는 메소드를 추상 클래스에서 선언**해 놓으면, 이 **클래스를 상속 받는 모든 클래스에서 해당하는 추상 클래스를 반드시 재정의**를 ****해야한다.
- **상속을 위한 클래스이므로 인스턴스를 따로 생성할 수 없다. ( new 생성 불가)**

# **사용 목적**

### ① 공통된 필드와 메소드를 통일

- **중복으로 사용하는 필드와 메소드를 제거하여 유지보수가 편하다.**

### ② 구현의 강제성을 이용한 기능 보장

- 해당 프로그램의 **기능에 필요한 메소드들을 잊고 코딩하지 않는다면 나중에 문제**가 생길 수도 있다. **그러나 추상 클래스를 상속**받는다면 **해당 클래스의 메소드들을 전부 구현**해야하기 때문에 **기능들을 보장받을 수 있다.**

### ③ 규격에 맞는 설계 구현

- **존재하는 제품을 개발자 마음대로 구현한다면 불량(에러)이 생길 수도 있기 때문에 해당 제품의 설계서에 따른 규격에 맞게 구현**해야 한다.

---

# **사용 예제**

- **예시**
    
    ```java
    abstract class 클래스명{
    	접근제어자 자료형 변수명;
    	접근제어자 abstract 리턴타입 메소드명();
    	접근제어자 리턴타입 메소드명();
    	...
    }
    ```
    
- **코드**
    
    ```java
    abstract class AbTest {
    	public int currentSpeed;
    
    	public AbTest(int speed) {    // 기본 생성자
    		this.currentSpeed = speed;
    	}
    	public void drive() {
    		System.out.println("전진");
    	}
    	public void stop() {
    		System.out.println("정지");
    	}
    	public abstract void bbang();  // 자동차 경적음 추상 메소드화
    }
    ----------------------------------------
    class Test extends AbTest {     // 추상 클래스 상속
    	public Test(int speed) {    // 기본 생성자
    		// super 키워드로 추상 클래스 기본 생성자 이용
    		super(speed);
    	}
    	public void showInfo() {
    		System.out.printf("Car의 현재 속도 : %d \n", this.currentSpeed);
    	}
    	@Override
    	public void bbang() {       // 추상 클래스 메소드를 상속받아 오버라이딩
    		System.out.println("빠----앙!!"); // 자동차 경적음 지정
    	}
    }
    ----------------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		Test tCar = new Test(100);
    		tCar.drive();
    		tCar.showInfo();
    		tCar.bbang();
    		tCar.stop();
    	}
    }
    ```
    
- **결과**
    
    ![](/Images/2023/08/JAVA-추상클래스(AbstractClass)/Untitled.png)