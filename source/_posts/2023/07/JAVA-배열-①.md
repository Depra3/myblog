---
title: JAVA - 배열 - ① 1차원 배열
date: 2023/07/20 21:00:00
categories:
- JAVA
tags:
- 개념
- 배열
- 1차원 배열
---

# 배열 정의

- **동일한 데이터 타입의 여러 데이터를 하나의 묶음으로 다루는 것**이다.

# 1 차원 배열

- **선형 구조로 이루어진 묶음**이다.

| a[0] | a[1] | a[2] | … |
| --- | --- | --- | --- |
| 일 | 이 | 삼 | … |

# 배열 선언 형식
- **예시**
```java
// ①
데이터타입[] 변수명 = new 데이터타입[길이];
데이터타입 변수명[] = new 데이터타입[길이];

// ②
데이터타입[] 변수명;
변수명 = new 데이터타입[] { 변수1, 변수2, ....};
데이터타입 변수명[];
변수명 = new 데이터타입[] { 변수1, 변수2, ....};

// ③
데이터타입[] 변수명 = { 변수1, 변수2, ....};
데이터타입 변수명[] = { 변수1, 변수2, ....};
```
#
- **코드**
    
    ```java
    // 방식 ①
    int[] a = new int[10];
    String aa[] = new String[10];
    
    // 방식 ②
    int[] b;
    b = new int[] {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
    String bb[];
    bb = new String[] {"일", "이", "삼", "사", "오", "육", "칠", "팔", "구", "십"};
    
    // 방식 ③
    int[] c = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
    String cc[] = {"일", "이", "삼", "사", "오", "육", "칠", "팔", "구", "십"};
    ```
    
#
- **출력**
    
    ```java
    // 방식 ① Arrays 클래스 사용
    System.out.println(Arrays.toString(b));
    System.out.println(Arrays.toString(bb));
    
    // 방식 ② 반복문 for 문 사용
    for (int i = 0; i < c.length; i++) {
    	System.out.println(c[i]);
    }
    System.out.println("--");
    
    // 방식 ③ 반복문 foreach 문 사용
    for (String arr : cc) {
    	System.out.println(arr);
    }
    ```
    - **방식 ③ 참고 : [Depra3's foreach 문](https://depra3.github.io/2023/07/21/2023/07/JAVA-반복문-foreach문/)**
#    
- **결과**
    
    ![](/Images/2023/07/JAVA-배열-①/Untitled.png)
    
---
# ★ 주의사항 ★

## 선언 시 주의할 점

```java
// error 발생 X
int[] c = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};

// error 발생 O
int[] d;
d = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
```

- 배열 c에서는 Error가 발생하지 않는다. 그러나 **배열 d와 같이 2 줄로 정의하면 컴파일 Error가 발생**한다.
    
    ![](/Images/2023/07/JAVA-배열-①/Untitled%201.png)
    

## 출력 시 주의할 점

```java
// 배열 내용 출력
System.out.println(Arrays.toString(b));
System.out.println(Arrays.toString(bb));

// 배열 주소 출력
System.out.println(c);
System.out.println(cc);
```

- **Arrays 클래스, 반복문을 이용하지 않고 그대로 변수명을 이용하여 출력하면 배열의 주소가 출력**이 된다.
    
    ![](/Images/2023/07/JAVA-배열-①/Untitled%202.png)