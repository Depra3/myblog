---
title: JAVA - 인터페이스(Interface)
date: 2023/08/28 21:00:00
categories:
- JAVA
tags:
- 개념
- 객체 지향 프로그래밍
- 패키지
- 추상 메소드
- 오버라이딩
- abstract
- static
- final
- 상속
---

# 인터페이스 (Interface)

- **클래스에서 특정한 기능(메소드)들을 모아 구현하도록 강제하는 기능**이 있다.

# 특징

- **추상 메소드와 상수**로 이루어져 있다.
- **생성자를 생성할 수 없다.**
- **다중 상속이 가능**하다.
- **상속 받은 클래스(하위)는 부모 인터페이스(상위)의 메소드들 모두 메소드 오버라이딩해야 한다.**

# 사용 목적

## ① **공통된 기능을 하는 메소드를 통일**

- **중복으로 기능하는 메소드들의 네이밍을 통일하여 소스 가독성과 유지보수가 편하다.**

## ② 구현의 강제성을 이용한 기능 보장

- 해당 프로그램의 **기능에 필요한 메소드들을 잊고 코딩하지 않는다면 나중에 문제**가 생길 수도 있다. **그러나 인터페이스를 상속**받는다면 **메소드들을 전부 구현하여야 하므로 기능을 보장할 수 있다.**

---

# 사용 예제

- **예시**
    
    ```java
    interface 인터페이스명 {
    	public 자료형 변수명 = 0;
    	public static 자료형 변수명 = "";
    	public static final 자료형 변수명 = "";
    	public void 메소드명();
    	public abstract void 메소드명();
    }
    ```
#    
- **코드**
    
    ```java
    interface InterfaceTest {
    	public static final String a = "Interface - Test";
    	public void show();
    	public abstract void view();
    }
    -------------------------------------
    class Test implements InterfaceTest {
    	@Override
    	public void show() {
    		System.out.println("Show!!");		
    	}
    	@Override
    	public void view() {
    		System.out.println("View!!");
    	}
    }
    -------------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		Test t1 = new Test();
    		System.out.println(t1.a); 
    		t1.show();
    		t1.view();
    	}
    }
    ```
#    
- **결과**
    
    ![](/Images/2023/08/JAVA-Interface/Untitled.png)
    

---

# **상속 : [Depra3's JAVA - Interface 상속](https://depra3.github.io/2023/08/23/2023/08/JAVA-%EC%83%81%EC%86%8D-Interface/)**