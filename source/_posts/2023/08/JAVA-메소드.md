---
title: JAVA - 메소드
date: 2023/08/04 21:30:00
categories:
- JAVA
tags:
- 개념
- 객체 지향 프로그래밍
- 메소드
- 메소드 오버로딩
---

# 메소드

- **멤버 함수 (member function)** 라고도 하며 객체 지향 프로그래밍에서 객체와 관련된 서브 루틴 ( 또는 함수) 이자 클래스가 갖고 있는 기능이다.
- **데이터와 멤버 변수에 대한 접근 권한을 갖는다.**

# 특징

- **메소드의 이름은 생성자와는 다르게 임의로 지정**할 수 있다.
- **하나의 클래스가 여러 개의 메소드를 가질 수 있다.**
    - **메소드 오버로딩을 이용하여 중복된 메소드명을 가진 메소드들을 가질 수 있다.**

# 사용 목적

- **중복되는 코드 사용을 줄여 반복적인 프로그래밍을 피할 수 있다.**
- 모듈화로 인해 **코드 가독성이 향상**된다.
- 모듈화로 인해 **유지 보수가 수월**해진다.

### 기본 구조

- **매개 변수 : 메소드에 전달된 입력 값을 저장하는 변수**
    ```java
    접근제어자(public, protect, private) 리턴타입(String, int, ...) 메소드명(자료형 매개변수①, 
                                                                          자료형 매개변수②, ...){
        ~~
        ~~
        return 리턴 값; // 단, 리턴타입이 void인 경우 return은 사용할 필요가 없다.
    }
    ```
#
---

# 메소드 종류

## 입력과 출력이 있는 메소드

- **매개 변수 a, b를 입력** 받아 **int형  a+b값을 return**한다.
#
- **코드**
    
    ```java
    int sum(int a, int b){
    	return a + b;
    }
    
    public static void main(String[] args) {
    	Test test = new Test();
    	int sum = test.sum(1, 2);
    	System.out.println("a와 b의 합 : " + sum);
    }
    ```
    
- **결과**
    
    ![](/Images/2023/08/JAVA-메소드/Untitled.png)
    

---

## 입력이 있지만 출력은 없는 메소드

- **매개 변수 a, b를 입력** 받지만 **return이 없다.**
- **출력값이 없어 메소드 자료형을 void로 한다.**
#
- **코드**
    
    ```java
    void sum(int a, int b){
    	System.out.println("a와 b의 합 : " + (a + b));
    }
    
    public static void main(String[] args) {
    	Test test = new Test();
    	test.sum(1, 2);
    }
    ```
    
- **결과**
    
    ![](/Images/2023/08/JAVA-메소드/Untitled%201.png)
    

---

## 입력이 없지만 출력이 있는 메소드

- **입력 받는 매개 변수가 없으나 String형 return값인 world을 출력**한다.
#
- **코드**
    
    ```java
    String hello(){
    	return "world"; // 리턴 값이 문자열이기 때문에 String 리턴 타입을 사용
    }
    
    public static void main(String[] args) {
    	Test test = new Test();
    	String re = test.hello();
    	System.out.println(re);
    }
    ```
    
- **결과**
    
    ![](/Images/2023/08/JAVA-메소드/Untitled%202.png)
    

---

## 입력과 출력이 없는 메소드

- **입력 값과 출력값이 없다.**
- **출력값이 없어 메소드 자료형을 void로 한다.**
#
- **코드**
    
    ```java
    void hello(){
    	System.out.println("world");
    }
    
    public static void main(String[] args) {
    	Test test = new Test();
    	test.hello();
    }
    ```
    
- **결과**
    
    ![](/Images/2023/08/JAVA-메소드/Untitled%203.png)