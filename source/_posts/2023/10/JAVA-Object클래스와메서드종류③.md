---
title: JAVA - Object 클래스와 메서드종류 ③ (equals, deppEquals)
date: 2023/10/02 20:30:00
categories:
- JAVA
tags:
- 개념
- Object 클래스
- 메서드 종류
- 객체 비교
- equals()
- deepEquals()
- 예제
---
<h1>
<details>
<summary>목차</summary>
<div markdown="1">

- [equals() 메서드](#equals-메서드)
- [deepEquals() 메서드](#deepEquals-메서드)
- [Objects 클래스의 equals와 deepEquals 차이](#Objects-클래스의-equals와-deepEquals-차이)
</div>
</details>
</h1>

---

# Object 클래스

> **모든 클래스들의 최상위 클래스
모든 클래스들은 상속하지 않아도 기본적으로 java.lang 패키지에 속한 Object클래스를 상속받고 Object클래스에 속한 메소드들을 사용할 수 있다.**
> 

---

## equals() 메서드

- **두 객체가 동등한지 비교하는 메서드**
#
- **예시**
    
    ```java
    Object 객체명1 = new Object();
    Object 객체명2 = new Object();
    
    // 방법 1 : 객체명1이 null인 경우 에러 발생으로 비교 불가
    객체명1.equals(객체명2);
    // 방법 2 : 방법 1과 달리 null 위치를 신경 쓸 필요가 없음
    Objects.equals(객체명1, 객체명2);
    ```
    
    - **객체명1 이 null인 경우**
        - **코드**
            
            ```java
            String str1 = "Depra3";
            String str2 = "Depra3";
            String str3 = null;
            System.out.println("str1.equals(str2) : " + str1.equals(str2));
            System.out.println("str3.equals(str2) : " + str3.equals(str2));
            ```
            
        - **결과**
            
            ![](/Images/2023/10/JAVA-Object클래스와메서드종류③/Untitled.png)
#  
- **코드**
    
    ```java
    // 방법 1
    Object obj1 = new Object();
    Object obj2 = new Object();
    System.out.println("obj1 : " + obj1);
    System.out.println("obj2 : " + obj2);
    System.out.println("obj1 == obj2 : " + (obj1 == obj2));
    System.out.println("---------------------------");
    
    String str1 = new String("Depra3");
    String str2 = new String("Depra3");
    System.out.println("str1 == str2 : " + (str1 == str2));
    System.out.println("str1.equals(str2) : " + str1.equals(str2));
    System.out.println("---------------------------");
    
    // 방법 2
    Integer o1 = 1000;
    Integer o2 = 1000;
    
    System.out.println(Objects.equals(o1, o2));
    System.out.println(Objects.equals(o1, null));
    System.out.println(Objects.equals(null, o2));
    System.out.println(Objects.equals(null, null));
    System.out.println("---------------------------");
    
    Integer[] arr1 = { 1, 2 };
    Integer[] arr2 = { 1, 2 };
    
    System.out.println(arr1);
    System.out.println(arr2);
    System.out.println(Objects.equals(arr1, arr2));
    ```
#
- **결과**
    
    ![](/Images/2023/10/JAVA-Object클래스와메서드종류③/Untitled%201.png)
    

---

## deepEquals() 메서드

- **equals() 메서드 보다 깊게 비교하는 메서드**
#
- **예시**
    
    ```java
    Object 객체명1 = new Object();
    Object 객체명2 = new Object();
    Objects.deepEquals(객체명1, 객체명2);
    ```
#
- **코드**
    
    ```java
    String str1 = new String("Depra3");
    String str2 = new String("Depra3");
    System.out.println(Objects.deepEquals(str1, str2));
    System.out.println(Objects.deepEquals(str1, null));
    System.out.println(Objects.deepEquals(null, null));
    System.out.println("---------------------------");
    
    Integer[] arr1 = { 1, 2 };
    Integer[] arr2 = { 1, 2 };
    
    System.out.println(Objects.deepEquals(arr1, arr2));
    System.out.println(Objects.deepEquals(null, arr2));
    System.out.println(Objects.deepEquals(null, null) + "\n");
    // 배열 비교
    System.out.println(Arrays.deepEquals(arr1, arr2));
    ```
#
- **결과**
    
    ![](/Images/2023/10/JAVA-Object클래스와메서드종류③/Untitled%202.png)
    

---

## Objects 클래스의 equals와 deepEquals 차이

- **코드**
    
    ```java
    String[][] str1 = new String[][] {{"a", "b"},{"c", "d"}};
    String[][] str2 = new String[][] {{"a", "b"},{"c", "d"}};
    System.out.println(Objects.equals(str1, str2));
    System.out.println(Objects.deepEquals(str1, str2));
    System.out.println("---------------------------");
    String[] str3 = new String[] {"a", "b"};
    String[] str4 = new String[] {"a", "b"};
    System.out.println(Objects.equals(str3, str4));
    System.out.println(Objects.deepEquals(str3, str4));
    ```
    
    - **equals()** 메서드는 **인자의 주소값을 비교**한다.
    - **deepEquals()** 메서드는 **객체를 재귀적으로 비교하여 다차원 배열 비교도 가능**하다.
#
- **결과**
    
    ![](/Images/2023/10/JAVA-Object클래스와메서드종류③/Untitled%203.png)