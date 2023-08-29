---
title: JAVA-연산자-③ 증감, 관계(비교)
date: 2023/07/10 21:00:00
categories:
- JAVA
tags:
- 개념
- 연산자
- 증감 연산자
- 관계(비교) 연산자
---

# 증감 연산자

- **변수의 값을 1 증가 또는 감소시키는 연산자**
| 연산자 기호 | 설명 |
| --- | --- |
| ++ | 1 증가 |
| -- | 1 감소 |
- **코드**
    
    ```java
    int a = 10;
    System.out.println("a = " + a);
    
    // a = a + 1; 와 같음
    a++;
    System.out.println("a++ => " + a);
    ++a;
    System.out.println("++a => " + a);
    
    // a = a - 1; 와 같음
    a--;
    System.out.println("a-- => " + a);
    --a;
    System.out.println("--a => " + a);
    ```
    
- **결과**

    ![](/Images/2023/07/JAVA-연산자-③/Untitled.png)
    
#
- **주의** : 증감 연산자 **위치에 따른 차이**가 있어서 **순서가 중요가 중요**하다.
    - **++a/—a** 인 경우 **증감하여 계산 후, 다른 연산자와 계산**
    - **a++/a—** 인 경우 **다른 연산자와 계산 후, 증감하여 계산**
    #
    - **코드**
        
        ```java
        // 증감 먼저 계산 후 다른 연산자와 계산
        int b = 9;
        int c = ++b * 10;
        System.out.println("b = " + b);
        System.out.println("++b * 10 = " + c);
        
        // 다른 연산자와 계산 후 다른 연산자와 계산
        int d = 9;
        int e = d++ * 10;
        System.out.println("d = " + d);
        System.out.println("d++ * 10 = " + e);
        ```
        
    - **결과**
        
        ![](/Images/2023/07/JAVA-연산자-③/Untitled%201.png)

---

# 관계(비교) 연산자

- **2개의 값의 관계를 비교하여 true, false를 판별한다.**

## **크기 비교**

| 연산자 기호 | 설명 |
| --- | --- |
| > | 좌측 값이 우측 값보다 크면 true, 아니면 false |
| >= | 좌측 값이 우측 값보다 크거나 같으면 true, 아니면 false |
| < | 좌측 값이 우측 값보다 작으면 true, 아니면 false |
| <= | 좌측 값이 우측 값보다 작거나 같으면 true, 아니면 false |
- **코드**
    
    ```java
    System.out.println("3 > 2 = " + (3>2));
    System.out.println("3 > 3 = " + (3>3));
    System.out.println("2 > 3 = " + (2>3));
    System.out.println("-------------");
    System.out.println("3 >= 2 = " + (3>=2));
    System.out.println("2 >= 2 = " + (2>=2));
    System.out.println("1 >= 2 = " + (1>=2));
    System.out.println("-------------");
    System.out.println("3 < 2 = " + (3<2));
    System.out.println("3 < 3 = " + (3<3));
    System.out.println("2 < 3 = " + (2<3));
    System.out.println("-------------");
    System.out.println("3 <= 2 = " + (3<=2));
    System.out.println("2 <= 2 = " + (2<=2));
    System.out.println("1 <= 2 = " + (1<=2));
    ```
    
- **결과**
    
    ![](/Images/2023/07/JAVA-연산자-③/Untitled%202.png)
    

## **동등 비교**

| 연산자 기호 | 설명 |
| --- | --- |
| == | 좌측 값과 우측 값이 같으면 true, 아니면 false |
| != | 좌측 값과 우측 값이 다르면 true, 아니면 false |
- **코드**
    
    ```java
    System.out.println("1 == 1 = " + (1==1));
    System.out.println("1 == 2 = " + (1==2));
    System.out.println("-------------");
    System.out.println("1 != 1 = " + (1!=1));
    System.out.println("1 != 2 = " + (1!=2));
    ```
    
- **결과**
    
    ![](/Images/2023/07/JAVA-연산자-③/Untitled%203.png)
    
---
# 문자 비교

- 문자 비교시 **아스키 코드에 기반하여 비교**를 한다.
    - 참고 : [아스키 코드(ASCII)](https://ko.wikipedia.org/wiki/ASCII)
    #
- **코드**
    
    ```java
    char a = 'A';
    char b = 'B';
    // A > B 일 때, false 출력
    System.out.println("A > B = " + (a>b));
    // 간단하게 A와 B의 차이 출력 => -1이 출력되어 1의 차이인 것을 확인 할 수 있다
    System.out.println(a-b);
    
    // 정수형으로 형변환 하여 출력 => A = 65, B = 66인 것을 알 수 있다.
    int c = (int)a;
    int d = (int)b;
    System.out.println("A = " + c);
    System.out.println("B = " + d);
    ```
    
- **결과**
    
    ![](/Images/2023/07/JAVA-연산자-③/Untitled%204.png)