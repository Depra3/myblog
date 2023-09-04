---
title: JAVA - 예외처리 (try ~ catch ~ finally 문)
date: 2023/09/03 21:30:00
categories:
- JAVA
tags:
- 개념
- Exception
- try
- catch
- finally
- 예제
---
<h1>
<details>
<summary>목차</summary>
<div markdown="1">

- [예외 ㅡ Exception](#예외-ㅡ-Exception)
- [try ㅡ catch ㅡ finally문](#try-ㅡ-catch-ㅡ-finally문)
- [사용 예제 ①](#사용-예제-①)
- [사용 예제 ②](#사용-예제-②)
</div>
</details>
</h1>
---

# 예외 ㅡ Exception

- **프로그램에 대한 사용자의 조작 또는 개발자의 코딩에서 문제가 발생하여 생기는 오류**
- **정의 및 종류 : [Depra3's JAVA - 예외(Exception) 정의 및 종류](https://depra3.github.io/2023/08/31/2023/08/JAVA-%EC%98%88%EC%99%B8(Exception)_%EC%A0%95%EC%9D%98_%EB%B0%8F_%EC%A2%85%EB%A5%98/)**

---
# **try ㅡ catch ㅡ finally문**

### try 블록

- **예외가 발생할 가능성이 있는 코드들을 묶는다.**

### catch 블록

- **예외가 발생하면 처리하는 코드들을 묶는다.**
- **발생하는 예외 종류에 따라 매개변수로 설정하여 종류에 따른 예외 처리를 할 수 있다.**
- **어디서 예외가 발생했는지 알기 위해 로그를 남기기도 한다.**

### finally 블록

- **예외 발생 유무에 상관없이 무조건 실행하는 코드들을 묶는다.**
- **생략이 가능하다.**
---

# 사용 예제 ①

- **예외 종류에 맞게 catch 블록에서 매개변수로 받아 사용**
#
- **예시**
    
    ```java
    try {
    	예외가 발생할 가능성이 있는 코드들
    } catch(예외 종류){
    	예외가 발생하면 처리하는 코드들
    } finally{ // 생략 가능
    	예외 상관없이 무조건 실행하는 코드들
    }
    ```
#    
- **코드**
    
    ```java
    public class Human {
    	public String name;
    
    	public Human(String name) {
    		this.name = name;
    	}
    
    	public void run() {
    		System.out.println("달리다.");
    	}
    }
    ---------------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		try {
    			Human h1 = new Human("Depra3");
    			System.out.println(h1);
    			h1.run();
    			
    			h1 = null;
    			System.out.println(h1);
    			h1.run();	// NullpointerException 예외 발생
    			
    		} catch (NullPointerException ne) {
    			System.out.println();
    			System.out.println("예외 발생!! Catch 블록 실행!!");
    			System.out.println("ne : " + ne);
    			System.out.println(ne.getStackTrace());
    			System.out.println(ne.getMessage());
    		} finally {
    			System.out.println();
    			System.out.println("Finally 블록 실행!!");
    		}
    	}
    }
    ```
#    
- **결과**
    
    ![](/Images/2023/09/JAVA-예외처리(try~catch~finally)/Untitled.png)
    

# 사용 예제 ②

- **예외 발생 종류와 상관 없이 catch 블록에서 Exception 클래스 객체를 매개변수로 받아 사용**
#
- **코드**
    
    ```java
    public class Human {
    	public String name;
    
    	public Human(String name) {
    		this.name = name;
    	}
    
    	public void run() {
    		System.out.println("달리다.");
    	}
    }
    ---------------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		try {
    			Human h1 = new Human("Depra3");
    			System.out.println(h1);
    			h1.run();
    			
    			h1 = null;
    			System.out.println(h1);
    			h1.run();	// NullpointerException
    			
    		} catch (Exception e) {
    			System.out.println();
    			System.out.println("예외 발생!! Catch 블록 실행!!");
    			System.out.println("e : " + e);
    			System.out.println(e.getStackTrace());
    			System.out.println(e.getMessage());
    		} finally {
    			System.out.println();
    			System.out.println("Finally 블록 실행!!");
    		}
    	}
    }
    ```
#    
- **결과**
    
    ![](/Images/2023/09/JAVA-예외처리(try~catch~finally)/Untitled%201.png)