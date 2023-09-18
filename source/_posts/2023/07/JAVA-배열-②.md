---
title: JAVA - 배열 - ② 다차원 배열
date: 2023/07/24 21:00:00
categories:
- JAVA
tags:
- 개념
- 배열
- 다차원 배열
---
<h1>
<details>
<summary>목차</summary>
<div markdown="1">

- [배열 정의](#배열-정의)
- [다차원 배열](#다차원-배열)
- [배열 선언 형식](#배열-선언-형식)
- [주의할 점](#주의할-점)
</div>
</details>
</h1>
---

# 배열 정의

- **동일한 데이터 타입의 여러 데이터를 하나의 묶음으로 다루는 것**이다.

# 다차원 배열

- **배열 요소로 또 다른 배열을 가진 배열**이다.
- **ex) 2차원 배열**
    
    
    | a[0][0] | a[0][1] | a[0][2] | a[0][3] | … |
    | --- | --- | --- | --- | --- |
    | a[1][0] | a[1][1] | a[1][2] | a[1][3] | … |
    | a[2][0] | a[2][1] | a[2][2] | a[2][3] | … |

# 배열 선언 형식
- **예시**
```java
// ①
데이터타입[][] 변수명 = new 데이터타입[길이][길이];
데이터타입[] 변수명[] = new 데이터타입[길이][길이];
데이터타입 변수명[][] = new 데이터타입[길이][길이];

// ②
데이터타입[][] 변수명;
변수명 = new 데이터타입[][] { {변수1, 변수2, ....}, { 변수1, 변수2, .... } };
데이터타입[] 변수명[];
변수명 = new 데이터타입[][] { {변수1, 변수2, ....}, { 변수1, 변수2, .... } };
데이터타입 변수명[][];
변수명 = new 데이터타입[][] { {변수1, 변수2, ....}, { 변수1, 변수2, .... } };

// ③
데이터타입[][] 변수명 = { {변수1, 변수2, ....}, { 변수1, 변수2, .... } };
데이터타입[] 변수명[] = { {변수1, 변수2, ....}, { 변수1, 변수2, .... } };
데이터타입 변수명[][] = { {변수1, 변수2, ....}, { 변수1, 변수2, .... } };
```
#
- **코드**
    
    ```java
    // 방식 ①
    int[][] a = new int[3][3];
    double[] aa[] = new double[3][3];
    String aaa[][] = new String[3][3];
    
    // 방식 ②
    int[][] b;
    b = new int[][] {
    	{ 1, 2, 3, 4},
    	{ 2, 3, 4, 5}
    }; 
    double[] bb[];
    bb = new double[][] {
    	{ 1, 2, 3, 4},
    	{ 2, 3, 4, 5}
    };
    String bbb[][];
    bbb = new String[][] {
    	{ "일", "이", "삼", "사"},
    	{ "이", "삼", "사", "오"}
    };
    
    // 방식 ③
    int[][] c = {
    	{ 1, 2, 3, 4},
    	{ 2, 3, 4, 5}
    };
    double[][] cc = {
    	{ 1, 2, 3, 4},
    	{ 2, 3, 4, 5}
    };
    String ccc[][] = {
    	{ "일", "이", "삼", "사"},
    	{ "이", "삼", "사", "오"}
    };
    ```
    
#
- **출력**
    
    ```java
    // 방식 ① Arrays 클래스 사용
    
    System.out.println(Arrays.toString(b[0]));
    System.out.println(Arrays.toString(bb[0]));
    System.out.println(Arrays.toString(bbb[0]));
    System.out.println();
    
    // 방식 ② 반복문 for 문 사용
    for (int i = 0; i < c.length; i++) {
    	for (int j = 0; j < c[i].length; j++) {
    		System.out.print(c[i][j] + "  ");
    		System.out.print(cc[i][j] + "  ");
    		System.out.print(ccc[i][j]);
    		System.out.println();
    	}
    }
    System.out.println();
    
    // 방식 ③ 반복문 foreach 문 사용
    for (String[] str : ccc) {
    	for (String s : str) {
    		System.out.print(s + " ");
    	}
    	System.out.println();
    }
    ```
#    
- **결과**
    
    ![](/Images/2023/07/JAVA-배열-②/Untitled.png)
    
---
# 주의할 점

- **배열 요소에 배열이 있기 때문에, 1차원 배열처럼 출력하면 배열 주소가 출력**된다.
#
- **코드**
    
    ```java
    System.out.println(Arrays.toString(b));
    ```
#    
- **결과**
    
    ![](/Images/2023/07/JAVA-배열-②/Untitled%201.png)