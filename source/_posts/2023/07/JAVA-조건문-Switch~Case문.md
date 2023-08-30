---
title: JAVA-조건문-Switch~Case문
date: 2023/07/14 20:00:00
categories:
- JAVA
tags:
- 개념
- 조건문
- Switch~Case문
---

# 조건문

- **프로그램 흐름에 원하는 기준을 조건으로 분기를 추가하여 흐름을 제어**할 때 이용한다.
- **종류** : **if 문, if ~ else 문, if ~ else if ~ else 문, 중첩 if문, switch - case 문**

# Switch ~ Case 문

- `IF 문`과 같은 조건문이지만 **다양한 연산자들을 이용하여 조건식을 만들 수 있는 `IF 문`과 달리 특정 값일 때에 실행문을 실행**한다.

## 사용 형식
- **예시**
  ```java
  switch(변수) {
    case 값1:
      실행문;
      break;
    case 값2:
      실행문;
      break;
    default:
      실행문;
  }
  ```

  - `Switch ~ Case 문`은 **Switch 문 에 들어가는 변수를 Case 문 에서 조건을 만들어 특정 값을 지정**하면 **break 문 전까지 실행문을 실행**한다.
  - **만약 모든 Case 문의 조건에 충족되지 않는다면 default의 실행문을 실행**하게 된다.
#
- **코드**
    
    ```java
    int a = 1;
    switch (a) {
    	case 1: 
    		System.out.println("1");
    		System.out.println("1");
    		break;
    	case 2: {
    		System.out.println("2");
    		break;
    	}
    	default:
    		System.out.println("default");
    }
    ```
#
- **결과**
    
    ![](/Images/2023/07/JAVA-조건문-Switch~Case문/Untitled.png)
    
    - **IF 문과 달리 Case 문에서 블록기호 { } 를 사용하지 않아도 두 줄이상 사용이 가능**하다.
    - **참고 : [depra3's JAVA-조건문-IF문](https://depra3.github.io/2023/07/12/2023/07/JAVA-%EC%A1%B0%EA%B1%B4%EB%AC%B8-IF%EB%AC%B8/)**
    
---
## **※ 주의 사항 ※**

- **Case 문 처리 이후 break 문으로 마무리** 지어야 한다. **그렇지 않으면 break 문이 나올 때 까지 모든 Case문을 처리**한다.
- **만약 모든 Case 문에 break 문이 없다면, default 문의 실행문 까지 실행**한다.
#
- **코드**
    
    ```java
    int a = 1;
    switch (a) {
    	case 1: 
    		System.out.println("1");
    		System.out.println("1");
    	case 2: {
    		System.out.println("2");
    	}
    	default:
    		System.out.println("default");
    }
    ```
#
- **결과**
    
    ![](/Images/2023/07/JAVA-조건문-Switch~Case문/Untitled%201.png)