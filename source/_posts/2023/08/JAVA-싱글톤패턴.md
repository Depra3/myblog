---
title: JAVA - 싱글톤패턴
date: 2023/08/21 19:30:00
categories:
- JAVA
tags:
- 개념
- 소프트웨어 디자인 패턴
- 싱글톤 패턴
- 특징
- 문제점
- 객체 단 1개
---

# 싱글톤 패턴

- **소프트웨어 디자인 패턴 중의 하나**다.
- **객체의 인스턴스가 단 1개만 생성되는 패턴이다.**
- **객체를 static 키워드를 사용하여 정적 메모리(static)에 할당**한다.
- **접근제어자에 private로 설정하여 상속이 불가능**하다.

# 특징

- **하나의 인스턴스만을 사용**한다.
- **생성된 객체 하나만을 활용**하여 사용하기 때문에 **재사용이 가능**하여 **메모리의 낭비를 방지**한다.
- **객체가 정적 메모리에 할당**이 되기 때문에 **전역성을 가지게 되어 다른 객체 간의 공유가 쉽다.**

---

# 사용 예제

- **코드**
    
    ```java
    public class SingletonTest {
    	private static SingletonTest instance = new SingletonTest();
    	private int a = 0;
    
    	private SingletonTest() {
    	}
    	
    	public static SingletonTest getInstance() {
    		return instance;
    	}
    
    	public int getA() {
    		return a;
    	}
    
    	public void setA(int a) {
    		this.a = a;
    	}
    }
    ----------------------------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		SingletonTest s1 = SingletonTest.getInstance();
    		System.out.println("s1.a = " + s1.getA());
    		System.out.println("--------------------");
    		
    		// a값 수정
    		s1.setA(10);
    		System.out.println("s1.a = " + s1.getA());
    		
    		SingletonTest s2 = SingletonTest.getInstance();
    		System.out.println("s2.a = " + s2.getA());
    	}
    }
    ```
    
- **결과**

    ![](/Images/2023/08/JAVA-싱글톤패턴/Untitled.png)
    
    - **싱글톤 패턴의 특징으로 객체를 재생성해도 처음 생성했던 객체가 리턴**된다.
    - **s1 객체에서 값을 수정**했지만 **s2 객체에서도 같은 값을 공유하는 모습**이 보인다.
    

---

# 싱글톤 패턴 문제점

### 1. **테스트가 어렵다.**

- **싱글톤의 객체에 대한 의존성이 있는 클래스를 테스트 할 때** **싱글톤이 전역 상태를 유지**하기 때문에 **싱글톤의 객체 상태가 다른 테스트의 영향을 받는다.**

### 2. **내부 상태를 변경하기 어렵다.**

- **싱글톤 객체는 하나의 값을 공유**하기 때문에 **한 쪽에서 수정하면 다른 쪽도 같이 값이 바뀌어 상황에 유연하게 대처하기 어렵다.**

### 3. **객체 의존성이 높다.**

- **싱글톤의 객체는 전역 상태**이기 떄문에 **다른 객체들이 싱글톤 객체를 의존하는 경우**에 **객체 간의 결합도가 높아질 수 있다.**
- **높아지는 결합도로 인해 코드 유지보수가 어렵고 객체의 재사용성이 떨어질 수 있다.**