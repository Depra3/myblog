---
title: JAVA-조건문-IF문
date: 2023/07/12 21:00:00
categories:
- JAVA
tags:
- 개념
- 조건문
- IF문
---

# 조건문

- **프로그램 흐름에 원하는 기준을 조건으로 분기를 추가하여 흐름을 제어**할 때 이용한다.
- **종류** : **if 문, if ~ else 문, if ~ else if ~ else 문, 중첩 if문, switch - case 문**

### 블럭 { }

- **중괄호로 표현**하며, **여러 코드들을 하나로 묶어 블럭**처럼 만들어 준다.

---

# IF 문

- 조건식이 **참(true)인 경우**, 실행문을 실행한다.
- 조건식이 **거짓(false)인 경우**, 실행문을 실행하지 않는다.

## **사용 형식 ①**

```java
if( 조건식 ) {
	// 조건식이 참인 경우 실행되는 코드
	실행문;
	실행문;
	실행문;
	...
}
```

- **실행문이 두 줄 이상인 경우, 블록 기호 { } 를 생략할 수 없다.**
#
- **예시**
    
    ```java
    int a = 1;
    
    if (a > 0) {
    	System.out.println("a는 0이 아니다.");
    	System.out.println("a는 0보다 크다.");
    	System.out.println("a는 1이다.");
    }
    ```
    
- **결과**

    ![](/Images/2023/07/JAVA-조건문-IF문/Untitled.png)
    

## 사용 형식 ②

```java
// 두가지 형식으로 사용 가능하다.
// 1
if( 조건식 )
	실행문;

// 2
if( 조건식 )	실행문;
```

- **실행문이 한 줄인 경우, 블록 기호 { } 를 생략**할 수 있다.
#
- **예시**
    
    ```java
    int a = 1;
    
    if(a > 0) 
    	System.out.println("a=1");
    
    if(a > 0) System.out.println("a=1");
    ```
    
- **결과**
    
    ![](/Images/2023/07/JAVA-조건문-IF문/Untitled%201.png)
    
---

# IF ~ else 문

- 조건식에 대해 **참(true)이 아닌 경우에 실행할 코드들을 추가할 때 이용**
- 조건식이 **참(true)인 경우, else 앞의 { } 에서 실행문을 실행**한다.
- 조건식이 **거짓(false)인 경우, else 뒤의 { } 에서 실행문을 실행**한다.

## 사용 형식 ①

```java
if ( 조건식 ) {
	// 조건식이 참인 경우 실행되는 코드
	실행문;
	실행문;
} else {
	// 조건식이 거짓인 경우 실행되는 코드
	실행문;
	실행문;
}
```

- **실행문이 두 줄 이상인 경우, 블록 기호 { } 를 생략할 수 없다.**
#
- **예시**
    
    ```java
    int a = 0;
    if (a > 0) {
    	System.out.println("a는 0이 아니다.");
    	System.out.println("a는 0보다 크다.");
    	System.out.println("a는 1이다.");
    } else {
    	System.out.println("a는 0보다 크지 않다.");
    	System.out.println("a는 0일 수 있다.");
    }
    ```
    
- **결과**
    
    ![](/Images/2023/07/JAVA-조건문-IF문/Untitled%202.png)
    

## 사용 형식 ②

```java
if ( 조건식 ) 실행문;
else          실행문;
```

- **실행문이 한 줄인 경우, 블록 기호 { } 를 생략**할 수 있다.
#
- **예시**
    
    ```java
    int a = 0;
    		
    if (a > 0)	System.out.println("a는 0보다 크다.");			
    else		System.out.println("a는 0보다 크지 않다.");
    ```
    
- **결과**
    
    ![](/Images/2023/07/JAVA-조건문-IF문/Untitled%203.png)
    
---

# IF ~ else if ~ else 문

- 앞서 이용했던 IF ~ else 문에서 **조건식을 추가하여 조금 더 다양하게 분기를 나누고 싶을 때는 IF ~ else if ~ else 문을 이용**한다.
- **조건식 ① 에서 참인 경우 실행문 ① 실행, 거짓인 경우 조건식 ② 에서 참, 거짓을 구분**한다.
	**조건식 ② 에서** **참인 경우 실행문 ② 실행, 거짓인 경우 실행문 ③ 을 실행**한다.
    

## 사용 형식 ①

```java
if ( 조건식 ① ) {
	// 조건식 ① 이 참인 경우 실행되는 코드
	실행문;
	실행문;
} else if( 조건식 ② )	{
	// 조건식 ① 이 거짓, 조건식 ② 가 참인 경우 실행되는 코드
	실행문;
	실행문;
} else {
	// 조건식 ① 과 ② 가 참인 경우 실행되는 코드
	실행문;
	실행문;
}
```

- **실행문이 두 줄 이상인 경우, 블록 기호 { } 를 생략할 수 없다.**
#
- **예시**
    
    ```java
    int a = 0;
    if (a > 0) {
    	System.out.println("a는 0보다 크다.");
    	System.out.println("a는 0보다 크다.");
    } else if ( a == 0 ){
    	System.out.println("a는 0이다.");
    	System.out.println("a는 0이다.");
    } else {
    	System.out.println("a는 0보다 작다.");
    	System.out.println("a는 0보다 작다.");
    }
    ```
    
- **결과**
    
    ![](/Images/2023/07/JAVA-조건문-IF문/Untitled%204.png)
    

## 사용 형식 ②

```java
if ( 조건식 ① )		  실행문①;
else if( 조건식 ② )	실행문②;
else          			실행문③;
```

- **실행문이 한 줄인 경우, 블록 기호 { } 를 생략**할 수 있다.
#
- **예시**
    
    ```java
    int a = 0;
    if (a > 0)  		System.out.println("a는 0보다 크다.");			
    else if(a == 0)	System.out.println("a는 0이다.");
    else	      		System.out.println("0는 0보다 작다.");
    ```
    
- **결과**
    
    ![](/Images/2023/07/JAVA-조건문-IF문/Untitled%205.png)
    
---

# 중첩 IF 문

- **횟수 제한 없이 IF문을 중첩하여 사용**할 수 있다.
- 사용하는 IF문들 안에서 분기를 나누고 싶을 때 사용한다.

## 사용 형식

```java
if ( 조건식 ① ) {
	// 조건식 ① 이 참인 경우 실행되는 코드
	실행문;
	if ( 조건식 ② ) {
		// 조건식 ② 이 참인 경우 실행되는 코드
		실행문;
	} else if ( 조건식 ③ ) {
		// 조건식 ② 이 거짓, 조건식 ③ 이 참인 경우 실행되는 코드
		실행문;
	} else {
		// 조건식 ② 와 ③ 이 거짓인 경우 실행되는 코드
		실행문;
	}
} else if( 조건식 ④ )	{
	// 조건식 ① 이 거짓, 조건식 ④ 가 참인 경우 실행되는 코드
	실행문;
} else {
	// 조건식 ① 과 ④ 가 거짓인 경우 실행되는 코드
	실행문;
}
```
#
- **예시**
    
    ```java
    int a = 1;
    if (a > 0) {
    	System.out.println("a는 0보다 크다.");
    	System.out.println("a는 0보다 크다.");
    	if (a == 1) {
    		System.out.println("a == 1");
    	} else if (a == 2) {
    		System.out.println("a == 2");
    	} else {
    		System.out.println("a == ??");
    	}
    } else if ( a == 0 ){
    	System.out.println("a는 0이다.");
    	System.out.println("a는 0이다.");
    } else {
    	System.out.println("a는 0보다 작다.");
    	System.out.println("a는 0보다 작다.");
    }
    ```
    
- **결과**
    
    ![](/Images/2023/07/JAVA-조건문-IF문/Untitled%206.png)