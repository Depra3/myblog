---
title: JAVA-반복문-while문
date: 2023/07/15 21:00:00
categories:
- JAVA
tags:
- 개념
---

# 반복문

- **프로그램 흐름에서 일정 횟수를 반복하고 싶은 구간에 사용하는 제어문**이다.
- **종류 : while 문, do ~ while 문, for 문**

# while 문

- **while 문은 조건식이 참(true) 인 경우에 동작하는 반복문**이며, **거짓(false)이라면 반복하지 않고 while 문에서 빠져나와 그 다음 코드를 실행**한다.
#
## 사용 형식 ①

```java
while(조건식){
	실행문;
	실행문;
}
```

- **실행문이 두 줄 이상인 경우, 블록 기호 { } 를 생략**할 수 없다.
#
- **예시**
    
    ```java
    int a = 1;
    while (a <= 10) { 
    	System.out.println("a = " + a);
    	a++;
    }
    ```
#    
- **결과**
    
    ![](/Images/2023/07/JAVA-반복문-while문/Untitled.png)
    

## 사용 형식 ②

```java
while(조건식)
	실행문;
```

- **실행문이 한 줄인 경우, 블록 기호 { } 를 생략**할 수 있다.
- **실행문이 두 줄인 경우, 첫 줄만 반복**한다.
- `사용 빈도가 매우 낮다.`
#
- **예시**
    
    ```java
    int b = 1;
    while (b <= 10)
    	System.out.println("b = " + b++);
    ```
#    
- **결과**
    
    ![](/Images/2023/07/JAVA-반복문-while문/Untitled%201.png)