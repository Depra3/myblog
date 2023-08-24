---
title: JAVA - 상속 - Interface
date: 2023/08/23 21:30:00
categories:
- JAVA
tags:
- 개념
- 객체 지향 프로그래밍
- 상속
- 다중 상속
- 생성자
- 메소드
- 메소드 오버로딩
- this
- extends
- implements
---

# 상속

- **기존 클래스(상위/부모 클래스)의 필드와 메소드를 다른 클래스(하위 클래스)가 이어받아 사용할 수 있게 하는 기능**이다.
- **다형성, 캡슐화, 추상화와 같이 객체 지향 프로그래밍을 구성하는 특징 중 하나**다.
    - **객체 지향 프로그래밍 : [JAVA - 객체 지향 프로그래밍](https://depra3.github.io/2023/08/01/2023/08/JAVA-%EA%B0%9D%EC%B2%B4%EC%A7%80%ED%96%A5%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D/)**
- **클래스는 extends, 인터페이스는 implements 키워드를 사용하여 구현**한다.
- **클래스는 다중 상속 불가, 인터페이스는 다중 상속 가능**

# 특징

- **인터페이스의 변수와 메소드를 재사용할 수 있어 개발 시간이 단축**된다.
- **클래스와 인터페이스 간 계층적 분류 및 관리가 가능하여 유지보수에 용이**하다.

---

# 상속 선언

- **클래스와 인터페이스 간의 상속은 implements 키워드를 사용**한다.
#
- **예시**
    
    ```java
    interface 인터페이스명 {
    		...
    }
    ----------------------------------
    class 클래스명(하위) implements 인터페이스명{
    		...
    }
    ```
    
- **코드**
    
    ```java
    interface InterfaceTest {
    	public void showName();
    	public void showNumber();
    }
    ---------------------------------------------------------
    class Test implements InterfaceTest {
    	
    	String name;
    	int number;
    	
    	public Test(String name, int number) {
    		this.name = name;
    		this.number = number;
    	}
    	
    	@Override
    	public void showName() {
    		System.out.println("name : " + name);
    	}
    
    	@Override
    	public void showNumber() {
    		System.out.println("number = " + number);
    	}
    }
    ---------------------------------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		Test t1 = new Test("Depra3", 5);
    		t1.showName();   // 오버라이딩된 메소드 호출
    		t1.showNumber(); // 오버라이딩된 메소드 호출
    	}
    }
    ```
    
    - **메소드 오버라이딩 : [JAVA - 메소드](https://depra3.github.io/2023/08/04/2023/08/JAVA-%EB%A9%94%EC%86%8C%EB%93%9C/)**
#
- **결과**
    
    ![](\Images\2023\08\JAVA-상속-Interface/Untitled.png)
    

---

# 이중 상속

- **인터페이스간의 상속은 extends 키워드를 사용**한다.
#
- **예시**
    
    ```java
    interface 인터페이스명1 {
    		...
    }
    ----------------------------------
    interface 인터페이스명2 extends 인터페이스명1 {
    		...
    }
    ----------------------------------
    class 클래스명(하위) implements 인터페이스명2 {
    		...
    }
    ```
    
- **코드**
    
    ```java
    interface InterfaceTest2 {
    	public void showNumber();
    }
    ---------------------------------------------------------
    interface InterfaceTest1 extends InterfaceTest2{
    	public void showName();
    }
    ---------------------------------------------------------
    class Test implements InterfaceTest1 {
    	
    	String name;
    	int number;
    	
    	public Test(String name, int number) {
    		this.name = name;
    		this.number = number;
    	}
    	
    	@Override
    	public void showName() {
    		System.out.println("name : " + name);
    	}
    
    	@Override
    	public void showNumber() {
    		System.out.println("number = " + number);
    	}
    }
    ---------------------------------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		Test t1 = new Test("Depra3", 15);
    		t1.showName();   // 오버라이딩된 메소드 호출
    		t1.showNumber(); // 오버라이딩된 메소드 호출
    	}
    }
    ```
    
- **결과**
    
    ![](\Images\2023\08\JAVA-상속-Interface/Untitled%201.png)
    

---

# 다중 상속 선언

- **implements 키워드 뒤에 나열하여 사용**한다.
#
- **예시**
    
    ```java
    interface 인터페이스명1 {
    		...
    }
    ----------------------------------
    interface 인터페이스명2 {
    		...
    }
    ----------------------------------
    class 클래스명(하위) implements 인터페이스명1, 인터페이스명2 {
    		...
    }
    ```
    
- **코드**
    
    ```java
    interface InterfaceTest1 {
    	public void showName();
    }
    ---------------------------------------------------------
    interface InterfaceTest2 {
    	public void showNumber();
    }
    ---------------------------------------------------------
    class Test implements InterfaceTest1, InterfaceTest2 {
    	
    	String name;
    	int number;
    	
    	public Test(String name, int number) {
    		this.name = name;
    		this.number = number;
    	}
    	
    	@Override
    	public void showName() {
    		System.out.println("name : " + name);
    	}
    
    	@Override
    	public void showNumber() {
    		System.out.println("number = " + number);
    	}
    }
    ---------------------------------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		Test t1 = new Test("Depra3", 10);
    		t1.showName();   // 오버라이딩된 메소드 호출
    		t1.showNumber(); // 오버라이딩된 메소드 호출
    	}
    }
    ```
    
- **결과**
    
    ![](\Images\2023\08\JAVA-상속-Interface/Untitled%202.png)