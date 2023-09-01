---
title: JAVA - final - ②
date: 2023/08/11 20:00:00
categories:
- JAVA
tags:
- 개념
- 객체 지향 프로그래밍
- final
- 클래스
- 객체
- Error
---

# **final**

> **사전적 의미로 ‘결정적인’, ‘마지막의’로 쓰인다.
자바에서는 사전적 의미와 같이 초기값이 결정되면 최종 결정이 되어 더 이상 값을 수정할 수 없다.**
> 

# **특징**

- **변수, 메소드, 클래스, 객체, 인자값에 사용이 가능하다.**
- **변수에 사용하면 재할당이 불가능하여 수정이 불가능하다.**
- **메소드에 사용하면 메소드 오버라이딩이 불가능하다.**
- **클래스에 사용하면 해당 클래스는 상속할 수 없다. 따라서, 자식 클래스를 만들지 못 한다.**
- **메소드의 인자값에 사용하면 해당 인자값은 수정할 수 없다.**
- **객체 생성에 사용하면 해당 객체는 같은 타입으로 재생성이 불가능하다.
그러나 객체 내부 변수는 수정이 가능하다.**

# **사용 목적**

- **변하지 말아야하는 싶은 변수, 메소드, 클래스, 인자값이 있다면 final을 사용하여 코딩 시에 예상치 못한 수정이 되거나 하는 상황 없이 마음 편안하게 코딩할 수 있다**

---

# final 클래스

> **final 클래스는 상속할 수 없는 클래스**다.
**Setter를 이용해 클래스 필드를 재할당** 할 수 있다.
>
#
- **예시**
    
    ```java
    접근제어자 final class 클래스명 { }
    ```
#    
- **코드**
    
    ```java
    public final class Test {
    	String a = "Depra3";
    	
    	public void show() {
    		System.out.println(a);
    	}
    	
    	// getter / setter
    	public String getA() {
    		return a;
    	}
    	public void setA(String a) {
    		this.a = a;
    	}
    }
    ----------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		Test t1 = new Test();
    		t1.show();
    
    		t1.setA("Depra");
    		t1.show();
    	}
    }
    ```
#    
- **결과**
    
    ![](/Images/2023/08/JAVA-final-②/Untitled.png)
    

## **※ 오류 발생 ※**

- **final 클래스는 상속할 수 없는 클래스이기에 상속 시에 에러 발생**
#
- **코드**
    
    ```java
    public final class Test {
    	String a = "Depra3";
    	
    	public void show() {
    		System.out.println(a);
    	}
    }
    ----------------------------------
    public class Test1 extends Test {
    	String a = "Depra2";
    	
    	public void show() {
    		System.out.println("Depra3 = " + a);
    	}
    }
    ----------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		Test1 t1 = new Test1();
    		t1.show();
    	}
    }
    ```
    
    - **에러 발생 위치**
        
        ![](/Images/2023/08/JAVA-final-②/Untitled%201.png)
#        
- **결과**
    
    ![](/Images/2023/08/JAVA-final-②/Untitled%202.png)
    

---

# final 객체

> **객체 생성에 사용하면 해당 객체는 같은 타입으로 재생성이 불가능하다.
그러나 객체 내부 변수는 수정이 가능하다.**
>
#
- **예시**
    
    ```java
    final 클래스명 객체명 = new 클래스명(); 
    ```
#    
- **코드**
    
    ```java
    public final class Test {
    	String a = "Depra3";
    	
    	public void show() {
    		System.out.println(a);
    	}
    }
    ----------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		final Test t1 = new Test();
    		t1.show();
    	}
    }
    ```
#    
- **결과**
    
    ![](/Images/2023/08/JAVA-final-②/Untitled%203.png)
    

## **※ 오류 발생 ※**

- **객체 생성에 사용하면 해당 객체는 같은 타입으로 재생성이 불가능하여 재할당을 하면 에러가 발생한다.**
#
- **코드**
    
    ```java
    public final class Test {
    	String a = "Depra3";
    	
    	public void show() {
    		System.out.println(a);
    	}
    }
    ----------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		final Test t1 = new Test();
    		t1 = new Test();
    		t1.show();
    	}
    }
    ```
    
    - **에러 발생 위치**
        
        ![](/Images/2023/08/JAVA-final-②/Untitled%204.png)
        
#    
- **결과**
    
    ![](/Images/2023/08/JAVA-final-②/Untitled%205.png)
    
---

# 메소드 인자값에 final 사용

>**인자값에 final을 사용하면 final 인자값의 수정은 불가능**하다.
>
#
- **예시**
    
    ```java
    접근제어자 리턴타입 메소드명(final 자료형 변수명){ }
    ```
#    
- **코드**
    
    ```java
    public class Test {		
    	public final void show(final String a) {
    		System.out.println(a);
    	}
    }
    
    ------------------------------------
    
    public class Exam {
    	public static void main(String[] args) {
    		Test t1 = new Test();
    		t1.show("Depra3's result");
    	}
    }
    ```
    
- **결과**
    
    ![](/Images/2023/08/JAVA-final-②/Untitled%206.png)
    

# **※ 오류 발생 ※**

- **받은 인자값을 수정하려 하면 오류 발생**
#
- **코드**
    
    ```java
    public class Test {		
    	public final void show(final String a) {
    		a = "Depra3";
    		System.out.println(a);
    	}
    }
    
    ------------------------------------
    
    public class Exam {
    	public static void main(String[] args) {
    		Test t1 = new Test();
    		t1.show("Depra3's result");
    	}
    }
    ```
    
    - **오류 발생 위치**
        
        ![](/Images/2023/08/JAVA-final-②/Untitled%207.png)
#        
- **결과**
    
    ![](/Images/2023/08/JAVA-final-②/Untitled%208.png)