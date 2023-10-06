---
title: JAVA - Object 클래스와 메서드종류 ② (getClass)
date: 2023/09/25 20:30:00
categories:
- JAVA
tags:
- 개념
- Object 클래스
- 메서드 종류
- getClass()
- 예제
---
<h1>
<details>
<summary>목차</summary>
<div markdown="1">

- [Object 클래스](#Object-클래스)
- [getClass() 메서드](#getClass-메서드)

</div>
</details>
</h1>

---

# Object 클래스

> **모든 클래스들의 최상위 클래스
모든 클래스들은 상속하지 않아도 기본적으로 java.lang 패키지에 속한 Object클래스를 상속받고 Object클래스에 속한 메서드들을 사용할 수 있다.**
> 

---

## getClass() 메서드

- **객체의 클래스 정보를 알 수 있는 메서드로 Class타입의 객체로 정보를 담아 반환한다.**
    - **정보를 가지고 있는 Class타입의 객체는 클래스 정보에 접근 할 수 있는 메소드들을 가지고 있다.**
        - **getName() :  해당 객체의 클래스의 이름을 반환하는 메서드**
        - **getSuperclass() : 해당 객체의 상위 클래스의 이름을 반환하는 메서드**
        - **getDeclaredFields() : 해당 객체의 클래스에서 선언되어있는 멤버 변수명들을 배열로 반환하는 메서드**
        - **getDeclaredMethods() : 해당 객체의 클래스에 선언되어 있는 멤버 함수명들을 배열로 반환하는 메서드**
		#
        - **나머지 메서드들 보는 법**
			- **아래 이미지와 같이 “ . “을 입력하면 사용할 수 있는 메서드들이 보인다.**
            
            	![](/Images/2023/09/JAVA-Object클래스와메서드종류②/Untitled.png)
            
            
#
- **예시**
    
    ```java
    Object 객체명1 = new Object();
    Class 객체명2 = 객체명1.getClass(); // 객체명2에 객체명1의 클래스 정보를 담는다.
	객체명2.getName();
	객체명2.getSuperclass();
	객체명2.getDeclaredFields();
	객체명2.getDeclaredMethods();
	...
    ```
#
- **코드**
    
    ```java
    public class Human {
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
    
    	public void run() {
    		System.out.println(this.name + "이(가) 달리다.");
    	}
    }
    -----------------------------------------
    public static void main(String[] args) {
    	Human h1 = new Human("Depra3", 1, 2, 3);
    	Class c1 = h1.getClass();  // Class 객체 c1에 객체 h1의 클래스 정보를 담는다.
    
    	System.out.println(c1.getName());  // 객체 c1에 담긴 클래스 이름 출력
    	
    	Field[] f1 = c1.getDeclaredFields();
    	for (int i = 0; i < f1.length; i++) {
    		System.out.println("멤버 필드 " + i + " : " + f1[i]);
    	}   // 멤버 변수 출력
    	
    	Method[] m1 = c1.getDeclaredMethods();
    	for (int i = 0; i < m1.length; i++) {
    		System.out.println("멤버 메서드 " + i + " : " + m1[i]);
    	}   // 멤버 함수 출력
    }
    ```
#
- **결과**
    
    ![](/Images/2023/09/JAVA-Object클래스와메서드종류②/Untitled%201.png)