---
title: JAVA - static
date: 2023/08/09 20:00:00
categories:
- JAVA
tags:
- 개념
- 객체 지향 프로그래밍
- 클래스 로더
- 정적변수
- static
- 객체
- Error
---

# Static

> **‘정적인’, ‘고정된’ 이란 의미**를 가지고 있으며 **Static 키워드를 사용하여 변수와 메소드를 만들 수 있다.** 이 **static 변수, static 메소드**를 다른 말로 **정적 필드와 정적 메소드**라고도 하며 합쳐서 **정적 멤버** 또는 **클래스 멤버**라고 한다.
> 

# 특징

- **어떤 객체 또는 인스턴스에 소속되지 않고 클래스에 고정된 멤버**이다. 
따라서 **클래스 로더가 클래스를 로딩하면 클래스와 같이 메모리 영역에 할당되어 관리**된다. 
이로 인해 **클래스의 로딩이 끝나는 즉시 사용**할 수 있다.
- **동일 클래스 내에서 모든 객체(인스턴스)에서 공유하여 사용**한다.
- **클래스 당 하나만 생성**되며 **클래스 멤버**라고도 부른다.
- **static 메소드 안에서 static 멤버들만 사용 가능**하다.

# 사용 목적

- **모든 클래스에서 호출이 가능한 전역변수 또는 전역함수를 만들어서 사용**하기 위함
- **static 변수**는 **동일 클래스 내에서 모든 객체(인스턴스)에서 공유가 가능하여 필요할 때 사용**한다.

---
# Static(정적) 멤버 선언

- **예시**
    ```java
    // 정적 필드 선언
    static 자료형 변수명;
    static 자료형 변수명 = ~~;

    // 정적 메소드 선언
    접근제어자 static 자료형 리턴타입 메소드명(){}

    // 예시
    public static int sta_field = 0; // 정적 필드 선언
    public static void sta_method(){} // 정적 메소드 선언
    ```
#
- **사용 예시**
    
    ```java
    public class Test {	
    	public static int sta_field1 = 123;
    	public int sta_field2 = 456;
    }
    
    --------------------------------------------------
    
    public class Exam {
    	public static void main(String[] args) {
    		System.out.println(Test.sta_field1);
    		
    		Test t2 = new Test();
    		System.out.println(t2.sta_field2);
    	}
    }
    ```
#    
- **결과**
    
    ![](/Images/2023/08/JAVA-static/Untitled.png)
    
---
# ※ 주의 사항 ※

- **오류 코드**
    
    ```java
    public class Test {	
    	public static int sta_field1 = 123;
    	public int sta_field2 = 456;
    }
    
    --------------------------------------------------
    
    public class Exam {
    	public static void main(String[] args) {
    		System.out.println(Test.sta_field1);
    		
    		System.out.println(Test.sta_field2);
    	}
    }
    ```
    
    - **Test 클래스에서 변수 sta_field2는 정적 변수로 선언하지 않아 오류 발생**
#    
- **결과**
    
    ![](/Images/2023/08/JAVA-static/Untitled%201.png)
    
    - **정적 변수는 클래스 로더가 클래스를 로딩하면 같이 메모리가 할당**되기 때문에 **객체 생성을 하지 않아도 사용이 가능**하다.
    - **정적 변수 선언을 하지 않으면 메모리에 할당이 되지 않아 객체 생성하기 전에 호출할 수 없는 것 같다.**