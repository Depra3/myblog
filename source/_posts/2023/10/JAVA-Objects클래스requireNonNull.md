---
title: JAVA - Objects 클래스 - requireNonNull()
date: 2023/10/10 20:30:00
categories:
- JAVA
tags:
- 개념
- Objects 클래스
- requireNonNull()
- 명시성
- 빠른 실패
- Fail - Fast
- 예제
---
<h1>
<details>
<summary>목차</summary>
<div markdown="1">

- [Objects 클래스](#Objects-클래스)
- [requireNonNull() 메서드](#requirenonNull-메서드)
    - [사용 이유](#사용-이유)
    - [사용 예시](#사용-예시)
</div>
</details>
</h1>

---

# **Objects 클래스**

> **JAVA 7에서 추가된 유틸리티 클래스.
객체 비교, 해시코드 생성, null 여부 등 편리하게 사용하는 메서드들이 포함되어 있다.**
> 

---

# requireNonNull() 메서드

- **입력된 값이 Null 이라면 NullPointerException가 발생, Null이 아니라면 입력값 그대로 반환한다.**

## 사용 이유

- **명시성**
    - **일반적인 코드보다 가독성이 더 좋다.**
    
    ```java
    String str;
    Objects.requireNonNull(str);
    ```
    
    - **위와 같이 변수 str의 null 여부를 확인하여 사용한다는 것을 알 수 있다.**
#
- **빠른 실패 ( Fail - Fast )**
    - **문제가 발생한 경우 즉각적으로 파악한다.**
    
    ```java
    String str = null;
    method(str);
    ----------------------
    void method(String str) {
    	// NullPointerException 가능성이 있음
    	A a = new A(str);
    	
    	// Null 여부를 확인하여 빠르게 NullPointerException를 밠생
    	B b = new b(Objects.requireNonNull(str));
    }
    ```
    
#
## 사용 예시

- **예시**
    
    ```java
    객체 객체명1 = 입력값;
    객체 객체명2 = 입력값;
    try{
    	System.out.println(Objects.requireNonNull(객체명1));
    	System.out.println(Objects.requireNonNull(객체명2, null이면 전달할 메세지));
    } catch(Exception e) {
    	System.out.println(e.getMessage());
    }
    ```
    
- **코드**
    
    ```java
    public static void main(String[] args) {
    		String str1 = "Depra3";
    		String str2 = null;
    		try {
    			System.out.println(Objects.requireNonNull(str1));
    			System.out.println("------");
    			System.out.println(Objects.requireNonNull(str2));
    		}
    		catch (Exception e) {
    			System.out.println(e.getMessage());
    		}
    ```
    
- **결과**
    
    ![](/Images/2023/10/JAVA-Objects클래스requireNonNull/Untitled.png)