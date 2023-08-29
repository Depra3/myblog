---
title: JAVA - 반복문 - foreach 문
date: 2023/07/21 20:00:00
categories:
- JAVA
tags:
- 개념
- 반복문
- foreach문
---

# 반복문

- **프로그램 흐름에서 일정 횟수를 반복하고 싶은 구간에 사용하는 제어문**이다.
- **종류 : while 문, do ~ while 문, for 문, foreach 문**

# foreach 문

- **자바 1.5버전부터 foreach 기능 추가**
- **초기값, 리스트 or 배열를 앞에 정의하여 사용하는 반복문**이다.
- **리스트 목록을 받아 리스트 목록 개수만큼 반복문 안의 실행문을 실행**한다.

## 사용 형식
- **예시**
    ```java
    데이터 타입[] 변수명 ① = { ... };
    for ( 데이터타입 변수명 ②: 변수명 ①) {
        System.out.println(변수명 ②);
    }
    ```
#
- **코드**
    
    ```java
    String[] a = { "일", "이", "삼"};
    for (String str : a) {
    	System.out.println(str);
    }
    ```
#    
- **결과**
    
    ![](/Images/2023/07/JAVA-반복문-foreach문/Untitled.png)