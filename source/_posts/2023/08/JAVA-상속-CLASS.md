---
title: JAVA - 상속 - CLASS
date: 2023/08/22 21:00:00
categories:
- JAVA
tags:
- 개념
- 객체 지향 프로그래밍
- 생성자
- 메소드
- 메소드 오버로딩
- super
- this
- extends
---

# 상속

- **기존 클래스(상위/부모 클래스)의 필드와 메소드를 다른 클래스(하위 클래스)가 이어받아 사용할 수 있게 하는 기능**이다.
- **다형성, 캡슐화, 추상화와 같이 객체 지향 프로그래밍을 구성하는 특징 중 하나**다.
    - **객체 지향 프로그래밍 : [JAVA - 객체 지향 프로그래밍](https://depra3.github.io/2023/08/01/2023/08/JAVA-%EA%B0%9D%EC%B2%B4%EC%A7%80%ED%96%A5%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D/)**
- **클래스는 extends, 인터페이스는 implements 키워드를 사용하여 구현**한다.
- **클래스는 다중 상속 불가, 인터페이스는 다중 상속 가능**

# 특징

- **기존 클래스(상위/부모 클래스)의 변수와 메소드를 재사용할 수 있어 개발 시간이 단축**된다.
- **클래스 간 계층적 분류 및 관리가 가능하여 유지보수에 용이**하다.

---

# 상속 선언

- **예시**
    
    ```java
    class 클래스명(기존, 상위) {
    		...
    }
    ----------------------------------
    class 클래스명(하위) extends 상위 클래스명{
    		...
    }
    ```
    
- **코드**
    
    ```java
    class Test {
    	String name;
    	int number;
    	
    	public void tPrint() {
    		System.out.println("Hello World!");
    	}
    }
    ---------------------------------------------------------
    class Test1 extends Test {
    	
    	String loc;
    	
    	Test1(String name, int number, String loc) {
    		super.name = name;
    		super.number = number;
    		this.loc = loc;
    	}
    	
    	@Override
    	public void tPrint() {
    		System.out.println("name = " + name);
    		System.out.println("number = " + number);
    		System.out.println("loc = " + loc);
    	}
    }
    ---------------------------------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		Test1 t1 = new Test1("Depra3", 1, "A1");
    		t1.showInfo(); // 오버라이딩된 메소드 호출
    		t1.tPrint();   // 상위(부모) 클래스 메소드 호출
    	}
    }
    ```
    
    - **메소드 오버라이딩 : [JAVA - 메소드](https://depra3.github.io/2023/08/04/2023/08/JAVA-%EB%A9%94%EC%86%8C%EB%93%9C/)**
#
- **결과**
    
    ![](\Images\2023\08\JAVA-상속-CLASS/Untitled.png)
    

---

# 참고 키워드

- **참고 이미지**
    
    ![](\Images\2023\08\JAVA-상속-CLASS/Untitled%201.png)
    

## super 키워드

- **하위 or 자식 클래스에서 상위 or 부모 클래스를 가리킬 때 사용하는 키워드**이다.
- **상위 or 부모 클래스의 필드와 메소드에 접근할 때 사용**한다.

## this 키워드

- **하위 or 자식 클래스의 객체에서 객체 자기 자신을 참조할 때 사용**한다.