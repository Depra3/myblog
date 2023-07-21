---
title: JAVA - 반복문 - do ~ while 문
date: 2023/07/17 21:00:00
categories:
- JAVA
tags:
- 개념
- 반복문
- do~while문
---

# 반복문

- **프로그램 흐름에서 일정 횟수를 반복하고 싶은 구간에 사용하는 제어문**이다.
- **종류 : while 문, do ~ while 문, for 문, foreach 문**

# do ~ while 문

- **do ~ whilie 문은 { } 안의 실행문을 무조건 한번 실행한 후 조건식에서 참(true) /**
    **거짓(false)을 가려 참(true)인 경우 반복문을 실행하고 거짓(false)인 경우 반복문을 종료한다.**
#
## 사용 형식 ①

```java
do {
	실행문;
} while (조건식)
// 조건식이 참인 경우 반복문 실행, 거짓인 경우 반복문 실행하지 않음.
```
#
- **예시**
    
    ```java
    int a = 1;
    do {
    	System.out.println("a = " + a);
    	a++;
    } while (a==1);
    
    System.out.println("-----");
    
    int b = 1;
    do {
    	System.out.println("b = " + b);
    	b++;
    } while (b < 10);
    ```
#
- **결과**
    
    ![](/Images/2023/07/JAVA-반복문-do~while문/Untitled.png)
    
#
## 사용 형식 ②

```java
do 
	실행문;
while (조건식)
// 조건식이 참인 경우 반복문 실행, 거짓인 경우 반복문 실행하지 않음.
```

- **실행문이 한 줄인 경우, 블록 기호 { } 를 생략**할 수 있다.
- `실제로 사용하는 것을 본 적 없다.`
#
- **예시**
    
    ```java
    int a = 1;
    do
    	System.out.println("a = " + a++);
    while (a==1);
    
    System.out.println("-----");
    
    // 한 줄로 사용할 수도 있다.
    int b = 1;
    do System.out.println("b = " + b++); while (b < 10);
    ```
#    
- **결과**
    
    ![](/Images/2023/07/JAVA-반복문-do~while문/Untitled%201.png)