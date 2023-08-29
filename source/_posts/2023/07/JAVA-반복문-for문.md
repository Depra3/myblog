---
title: JAVA - 반복문 - for 문
date: 2023/07/18 21:00:00
categories:
- JAVA
tags:
- 개념
- 반복문
- For문
---

# 반복문

- **프로그램 흐름에서 일정 횟수를 반복하고 싶은 구간에 사용하는 제어문**이다.
- **종류 : while 문, do ~ while 문, for 문, foreach 문**

# for 문

- **초기값, 조건식, 증감식을 앞에 정의하여 한 눈에 보기 쉬운 형식의 반복문**이다.
- **초기값에서 증감식 ( ++ / -- 등 ) 에 따라 조건식이 참인 경우 반복문 안의 실행문을 실행**한다.

#
## 사용 형식
- **예시**
    ```java
    for(초기값; 조건식; 증감식) {
        실행문;
    }
    ```

    - **앞선 반복문(while, do ~ while)과 같이 실행문이 한 줄인 경우, 블록 기호 { } 생략 가능**하다.
    - **참고 : [depra3's 반복문 - do~while문](https://depra3.github.io/2023/07/17/2023/07/JAVA-%EB%B0%98%EB%B3%B5%EB%AC%B8-do~while%EB%AC%B8/)**
#
- **코드**
    
    ```java
    for (int i = 0; i < 10; i++) {
    	System.out.println("i = " + i);
    }
    ```
#
- **결과**
    
    ![](/Images/2023/07/JAVA-반복문-for문/Untitled.png)
    
---
# 중첩 for 문

- **for 문을 중첩해서 사용**할 수 있다.
#
## 사용 형식
- **예시**
    ```java
    for(초기값; 조건식; 증감식) {
        실행문;
        for(초기값; 조건식; 증감식) {
            실행문;
        }
        실행문;
    }
    ```

    - **원하는 만큼 중첩해서 사용**할 수 있다.
#
- **코드**
    
    ```java
    for (int i = 1; i < 11; i++) {
    	for (int j = 0; j < i; j++) {
    		System.out.print("*");
    	}
    	System.out.println();
    }
    ```
    
#
- **결과**
    
    ![](/Images/2023/07/JAVA-반복문-for문/Untitled%201.png)
    
    - **for (int j = 0; j < i; j++)** 에서 **j < i** 를 **j < 11 - i 로 변경하면 역으로 나열**된다.
        
        ![](/Images/2023/07/JAVA-반복문-for문/Untitled%202.png)