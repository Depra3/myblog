---
title: JAVA-데이터타입
date: 2023/06/28 21:00:00
categories:
- JAVA
tags:
- 개념
---

# **데이터 타입**
![](/Images/2023/06/JAVA-데이터타입/Untitled.png)

---
## **`정수형` 타입 선언 및 출력**

- byte, short, int, long타입들을 이용하며, 실수 입력 시에 오류가 발생한다.

- 코드
    
    ```java
    byte a = 1;
    short b = 2;
    int c = 3;
    long d = 4;
    
    System.out.println(a);
    System.out.println(b);
    System.out.println(c);
    System.out.println(d);
    ```
    

- 결과
    
    ![](/Images/2023/06/JAVA-데이터타입/Untitled%201.png)
    
---
## `문자형` 타입 선언 및 출력

- char타입이며 입출력 시에 ASCII를 참조한다.

- 코드
    
    ```jsx
    char a = 'a';
    char b = 65;
    
    System.out.println(a);
    System.out.println(b);
    ```
    
    - char타입에서는 작은 따옴표(’ ’)를 사용
        - 큰 따옴표(” ”)는 String객체를 이용하여 문자열 변수 선언시 사용

- 결과
    
    ![](/Images/2023/06/JAVA-데이터타입/Untitled%202.png)
    
    - char 타입에 숫자도 입력 받을 수 있으나 출력은 ASCII을 참조하여 출력한다.
        - 참고 자료 : [ASCII -위키백과](https://ko.wikipedia.org/wiki/ASCII)
    
---
## `논리형` 타입 선언 및 출력

- boolean타입이며 참(True 또는 1), 거짓(False 또는 0) 2가지 값을 사용한다.

- 코드
    
    ```jsx
    boolean a = true;
    boolean b = false;
    
    System.out.println(a);
    System.out.println(b);
    ```
    

- 결과
    
    ![](/Images/2023/06/JAVA-데이터타입/Untitled%203.png)
    
---
## `실수형` 데이터 타입

- 부동소수점 표현 방식을 사용
    - 부호 : 1bit에서 +를 0으로, -를 1로 표현한다.
    - 지수 : 지수부분을 표현
        - 예시 : $2^5$ 에서 5가 지수 부분
    - 가수 : 소수점 우측의 숫자 부분을 표현한다.
    - 참고 자료 : [부동소수점 - 위키백과](https://ko.wikipedia.org/wiki/%EB%B6%80%EB%8F%99%EC%86%8C%EC%88%98%EC%A0%90)
    
- 코드
    
    ```jsx
    float a = 1.5f;
    double b = 2.0;
    double c = 3.0d;
    
    System.out.println(a);
    System.out.println(b);
    System.out.println(c);
    ```
    
    - JAVA에서는 실수 선언 시에 double자료형을 기본으로 한다. ( →3.0d에서 d는 생략 가능)
        - 따라서, float 선언 부분에서 f가 붙는 이유이기도 하다.
    
- 결과
    
    ![](/Images/2023/06/JAVA-데이터타입/Untitled%204.png)