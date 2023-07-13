---
title: JAVA-연산자-④ 논리, 조건
date: 2023/07/11 21:00:00
categories:
- JAVA
tags:
- 개념
---

# 논리 연산자

- 2개의 boolean 값의 관계를 비교하여 true, false를 판별한다.
    - boolean : [데이터타입 - boolean(논리형)](https://depra3.github.io/2023/06/28/2023/06/JAVA-%EB%8D%B0%EC%9D%B4%ED%84%B0%ED%83%80%EC%9E%85/)
    
    ![](/Images/2023/07/JAVA-연산자-④/Untitled.png)
    

## 연산식

![](/Images/2023/07/JAVA-연산자-④/Untitled%201.png)

- **예시**

    ```java
    boolean a = true;
    boolean b = false;

    System.out.println("true  & true  = " + (a & a));
    System.out.println("true  & false = " + (a & b));
    System.out.println("false & true  = " + (b & a));
    System.out.println("false & false = " + (b & b));
    System.out.println("------------------------");
    System.out.println("true  && true  = " + (a && a));
    System.out.println("true  && false = " + (a && b));
    System.out.println("false && true  = " + (b && a));
    System.out.println("false && false = " + (b && b));
    System.out.println("------------------------");
    System.out.println("true  | true  = " + (a | a));
    System.out.println("true  | false = " + (a | b));
    System.out.println("false | true  = " + (b | a));
    System.out.println("false | false = " + (b | b));
    System.out.println("------------------------");
    System.out.println("true  || true  = " + (a || a));
    System.out.println("true  || false = " + (a || b));
    System.out.println("false || true  = " + (b || a));
    System.out.println("false || false = " + (b || b));
    System.out.println("------------------------");
    System.out.println("true  ^ true  = " + (a ^ a));
    System.out.println("true  ^ false = " + (a ^ b));
    System.out.println("false ^ true  = " + (b ^ a));
    System.out.println("false ^ false = " + (b ^ b));
    System.out.println("------------------------");
    System.out.println("!true = " + !a);
    System.out.println("!false = " + !b);
    ```
#
- **결과**
    
    ![](/Images/2023/07/JAVA-연산자-④/Untitled%202.png)

---

# 조건 연산자

- **조건식, true인 경우의 값, false인 경우의 값**을 필요로 하여 **총 3개의 피연산자가 있는 연산자**다.
    
    ```java
    조건식 ? true : false
    ```
#
- **예시**
    
    ```java
    // a는 5라고 정의
    int a = 5;
    
    String b = a % 2 == 0 ? "짝수" : "홀수";
    System.out.println("a는 " + b + "다");
    
    boolean c = a > 3 ? true : false;
    System.out.println("a는 3보다 크다. : " + c);
    
    // 조건식을 중첩으로 사용할 수도 있다.
    String d = a % 2 == 0 ? "짝수" : (a % 2 == 1 ? "홀" : "수"); 
    System.out.println(d);
    
    // 조건식을 조건문인 IF문으로 변환하여 사용 가능하다.
    // IF문에서 경우 조건식으로 바꾸어서 사용할 수 도 있다.
    boolean e;
    if (a>3) {
    	e = true;
    } else {
    	e = false;
    }
    System.out.println("a는 3보다 크다. : " + e);
    
    // 피연산자의 타입이 다른 경우 자동 타입 변환이 이루어진다.
    // a가 5보다 큰 경우 1.0 / 아닌경우 0 이지만 변수 f에 0.0이 대입된다.
    double f = a > 5 ? 1.0 : 0;
    System.out.println(f);
    ```
#    
- **결과**
    
    ![](/Images/2023/07/JAVA-연산자-④/Untitled%203.png)