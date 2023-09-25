---
title: JAVA - Object클래스 와 메서드종류 ①
date: 2023/09/23 20:00:00
categories:
- JAVA
tags:
- 개념
- Object 클래스
- 메서드 종류
- toString()
- hashCode()
- 예제
---
<h1>
<details>
<summary>목차</summary>
<div markdown="1">

- [Object 클래스](#Object-클래스)
- [메서드 종류](#메서드-종류)
    - [toString() 메서드](#toString-메서드)
    - [hashCode() 메서드](#hashCode-메서드)
</div>
</details>
</h1>
---

# Object 클래스

> **모든 클래스들의 최상위 클래스**
**모든 클래스들은 상속하지 않아도 기본적으로 java.lang 패키지에 속한 Object클래스를 상속받고 Object클래스에 속한 메서드들을 사용할 수 있다.**
> 

---

# 메서드 종류

## toString() 메서드

- **toString() 메서드는 객체를 문자열로 표현된 정보값으로 반환한다.**
#
- **예시**
    
    ```java
    // Object 클래스에 정의되어 있는 메서드 코드
    public String toString() {
        return getClass().getName() + "@" + Integer.toHexString(hashCode());
    }
    ----------------
    // 사용 예시
    객체.toString();
    ```
#
- **코드**
    
    ```java
    public static void main(String[] args) {
    	Object obj = new Object();
    	Date date = new Date();
    	
    	System.out.println(obj.toString());
    	System.out.println(date.toString());
    	// Date라는 클래스 안에는 toString이 오버라이딩이 되어 있다.
    	// 그래서 날짜 형식으로 출력이 된다.
    }
    ```
#
- **결과**
    
    ![](/Images/2023/09/JAVA-Object클래스와메서드종류①/Untitled.png)
    

---

## hashCode() 메서드

- **해시코드는 객체를 식별하는 하나의 정수 값을 말한다.**
- **따라서, hashCode() 메서드는 객체의 해시코드를 반환한다.**
#
- **예시**
    
    ```java
    // Object 클래스에 정의되어 있는 메서드 코드
    public native int hashCode();
    ----------------
    // 사용 예시
    객체.hashCoode();
    ```
    
    - **hashCode() 메서드의 내용이 없는 것처럼 보인다. 그러나 C언어로 작성한 native함수로 정의되어있는 것 같다.**
        - **자세한 설명은 [링크](https://srvaroa.github.io/jvm/java/openjdk/biased-locking/2017/01/30/hashCode.html)를 참고.**
#
- **코드**
    
    ```java
    public class Human {
    	public String name;
    
    	public Human(String name) {
    		this.name = name;
    	}
    
    	public void run() {
    		System.out.println(this.name + "이(가) 달리다.");
    	}
    }
    ---------------------
    public class Exam {
    	public static void main(String[] args) {
    		Human h1 = new Human("Depra3");
    		
    		System.out.println(h1);  // 객체 h1의 주소
    		System.out.println(h1.hashCode());
    	}
    }
    ```
#
- **결과**
    
    ![](/Images/2023/09/JAVA-Object클래스와메서드종류①/Untitled%201.png)