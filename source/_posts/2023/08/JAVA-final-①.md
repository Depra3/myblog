---
title: JAVA - final - ①
date: 2023/08/10 20:00:00
categories:
- JAVA
tags:
- 개념
- 객체 지향 프로그래밍
- final
- 변수
- 필드
- 함수
- 메소드
- Error
---

# **final**

> **사전적 의미로 ‘결정적인’, ‘마지막의’로 쓰인다.**
**자바에서는 사전적 의미와 같이 초기값이 결정되면 최종 결정이 되어 더 이상 값을 수정할 수 없다.**
> 

# **특징**

- **변수, 메소드, 클래스, 객체에 사용이 가능하다.**
- **변수에 사용하면 재할당이 불가능하여 수정이 불가능하다.**
- **메소드에 사용하면 메소드 오버라이딩이 불가능하다.**
- **클래스에 사용하면 해당 클래스는 상속할 수 없다. 따라서, 자식 클래스를 만들지 못 한다.**
- **객체 생성에 사용하면 해당 객체는 같은 타입으로 재생성이 불가능하다.
그러나 객체 내부 변수는 수정이 가능하다.**

# **사용 목적**

- **변하지 말아야하는 싶은 변수, 메소드, 클래스가 있다면 final을 사용하여 코딩 시에 예상치 못한 수정이 되거나 하는 상황 없이 마음 편안하게 코딩할 수 있다.**

---

# **final 변수**

- **예시**
    
    ```java
    // 형식 ①
    final 자료형 변수명;
    변수명 = ~~;
    
    // 형식 ②
    final 자료형 변수명 = ~~;
    ```
    
- **코드**
    
    ```java
    final int a;
    a = 1;
    final String b = "Depra3";
    System.out.println(a);
    System.out.println(b);
    ```
    
- **결과**
    
    ![](/Images/2023/08/JAVA-final-①/Untitled.png)
    

### **※ 오류 발생 ※**

- **final 변수에 재할당 시에 오류 발생**

- **코드**
    
    ![](/Images/2023/08/JAVA-final-①/Untitled%201.png)
    
- **결과**
    
    ![](/Images/2023/08/JAVA-final-①/Untitled%202.png)
    

---

# final 메소드

- **final 메소드는 변경을 원치 않는 메소드를 선언할 때 사용**한다.
- **메소드 오버라이딩이 불가능하여 오버라이딩 한다면 오류가 발생**한다.

- **예시**
    
    ```java
    접근제어자 final 리턴타입 메소드명(){ }
    ```
    
- **코드**
    
    ```java
    public class Test {
    	String a = "Depra3";
    		
    	public final void show() {
    		System.out.println(a);
    	}
    }
    
    ------------------------------------
    
    public class Exam {
    	public static void main(String[] args) {
    		Test t11 = new Test();
    		t11.show();
    	}
    }
    ```
    
- **결과**
    
    ![](/Images/2023/08/JAVA-final-①/Untitled%203.png)
    

### **※ 오류 발생 ※**

- **final 메소드에 오버라이딩 시에 오류 발생**
- **코드**
    
    ```java
    public class Test {
    	String a = "Depra3";
    		
    	public final void show() {
    		System.out.println(a);
    	}
    }
    ------------------------------------
    public class Test1 extends Test {
    	String a = "Depra2";
    	
    	public void show() { // 메소드 오버라이딩 오류 발생
    		System.out.println("Depra3 = " a);
    	}
    }
    ------------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		Test1 t11 = new Test1();
    		t11.show();
    	}
    }
    ```
    
- **결과**
    
    ![](/Images/2023/08/JAVA-final-①/Untitled%204.png)