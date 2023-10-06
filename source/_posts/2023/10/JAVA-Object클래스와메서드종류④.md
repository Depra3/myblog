---
title: JAVA - Object 클래스와 메서드종류 ④ (clone() - 얕은 복사, 깊은 복사)
date: 2023/10/06 20:30:00
categories:
- JAVA
tags:
- 개념
- Object 클래스
- 메서드 종류
- 객체 복사
- clone()
- 얕은 복사
- 깊은 복사
- 예제
---
<h1>
<details>
<summary>목차</summary>
<div markdown="1">

- [Object 클래스](#Object-클래스)
- [clone() 메서드](#clone-메서드)
- [얕은 복사와 깊은 복사](#얕은-복사와-깊은-복사)
	- [얕은 복사](#얕은-복사)
	- [깊은 복사](#깊은-복사)
</div>
</details>
</h1>

---

# Object 클래스

> **모든 클래스들의 최상위 클래스
모든 클래스들은 상속하지 않아도 기본적으로 java.lang 패키지에 속한 Object클래스를 상속받고 Object클래스에 속한 메소드들을 사용할 수 있다.**
> 

---

## clone() 메서드

- **객체의 복제를 하기 위한 메서드로 해당 객체를 복제하여 새로운 객체를 생성한다.**
#
- **예시**
    
    ```java
    try{
    	객체 객체명1 = new 객체(...);
    	객체 객체명2 = (객체) 객체명1.clone();
    } catch(Exception e) {}
    ```
    #
    - **메서드 오버라이딩**
        
        ```java
        class 클래스명 implements Cloneable {
        	
            // clone() 메서드 오버라이딩
            public Object clone() throws CloneNotSupportedException {
        		// CloneNotSupportedException는 checked exception이기에 반드시 예외처리 해야함
                return super.clone(); // 부모의 clone을 그대로 불러와 반환
            }
        }
        ```
#        
- **코드**
    
    ```java
    public class Human implements Cloneable {
    	public String name;
    	public int age;
    	public int height;
    	public int weight;
    
    	public Human(String name, int age, int height, int weight) {
    		this.name = name;
    		this.age = age;
    		this.height = height;
    		this.weight = weight;
    	}
    	
    	@Override
    	protected Object clone() throws CloneNotSupportedException {
    		return super.clone();
    	}
    }
    ----------------------------------------------------
    public class Main {
      public static void main(String[] args) {
    		try {
    			Human h1 = new Human("Depra3", 10, 20, 30);
    			Human h2 = (Human) h1.clone();
    			
    			System.out.println(h1);
    			System.out.println(h2);
    			
    			System.out.println(h1.name);
    			System.out.println(h2.name);
    			
    			System.out.println(h1.age);
    			System.out.println(h2.age);
    			
    			System.out.println(h1.height);
    			System.out.println(h2.height);
    			
    			System.out.println(h1.weight);
    			System.out.println(h2.weight);
    		} catch (Exception e) {	}
    	}
    }
    ```
#
- **결과**
    
    ![](/Images/2023/10/JAVA-Object클래스와메서드종류④/Untitled.png)
    

---

# 얕은 복사와 깊은 복사

## 얕은 복사

- **복사할 때 해당 객체의 주소값을 참조한다. 그로 인해 복사된 객체는 원본 객체에 종속적이다.**
- **call by reference (참조에 의한 호출) 개념과 비슷하다.**
#
- **코드**
    
    ```java
    public class Main {
      public static void main(String[] args) {
    		try {
    			Human h1 = new Human("Depra3", 10, 20, 30);
    			Human h1_cp = h1;
    			
    			// 복사된 객체에서 30을 50으로 값 변경
    			h1_cp.weight = 50;
    			
    			// 원본 객체와 복사된 객체의 주소값이 같음
    			System.out.println(h1);
    			System.out.println(h2);
    			
    			System.out.println(h1.name);
    			System.out.println(h2.name);
    			
    			System.out.println(h1.age);
    			System.out.println(h2.age);
    			
    			System.out.println(h1.height);
    			System.out.println(h2.height);
    			
    			// 변경된 값 50 출력
    			System.out.println(h1.weight);
    			System.out.println(h2.weight);
    		} catch (Exception e) {	}
    	}
    }
    ```
#    
- **결과**
    
    ![](/Images/2023/10/JAVA-Object클래스와메서드종류④/Untitled%201.png)
    

## 깊은 복사

- **복사할 때 해당 객체의 주소값이 아닌 객체안의 필드와 메서드들을 모두 복사하여 원본 객체와 독립적인 객체를 생성한다.**
- **call by values (값에 의한 호출) 개념과 비슷하다.**
#
- **코드**
    
    ```java
    public class Main {
      public static void main(String[] args) {
    		try {
    			Human h1 = new Human("Depra3", 10, 20, 30);
    			Human h1_cp = (Human) h1.clone();
    			
    			// 복사된 객체에서 30을 50으로 값 변경
    			h1_cp.weight = 50;
    			
    			// 원본 객체와 복사된 객체의 주소값이 다름
    			System.out.println(h1);
    			System.out.println(h2);
    			
    			System.out.println(h1.name);
    			System.out.println(h2.name);
    			
    			System.out.println(h1.age);
    			System.out.println(h2.age);
    			
    			System.out.println(h1.height);
    			System.out.println(h2.height);
    			
    			// 원본 30, 복사 50 출력
    			System.out.println(h1.weight);
    			System.out.println(h2.weight);
    		} catch (Exception e) {	}
    	}
    }
    ```
#    
- **결과**
    
    ![](/Images/2023/10/JAVA-Object클래스와메서드종류④/Untitled%202.png)