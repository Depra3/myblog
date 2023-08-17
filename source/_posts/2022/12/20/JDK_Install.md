---
title: JDK 설치 및 환경 변수 설정
date: 2022/12/19 18:00:00
categories:
- JAVA
tags:
- JAVA
- JDK
---

# JDK 설치

## ★ 다운로드 링크 ★ 
## **[JDK 설치](https://www.oracle.com/kr/java/technologies/downloads/)**
#
- **Java 17 -> Windows -> 원하는 설치 방식으로 다운로드**
  (zip이 편한 것 같아서 zip을 선택했습니다.)
    
    ![](/Images/2022/12/20/JDK_Install/Untitled.png)
#    
- 이와 같이 **원하는 폴더 안에 압축해제**
    
    ![](/Images/2022/12/20/JDK_Install/Untitled%201.png)
    

# 환경  변수 설정

- **내 PC에서 마우스 오른쪽 클릭 후 속성 클릭**
    
    ![](/Images/2022/12/20/JDK_Install/Untitled%202.png)
#    
- **고급 시스템 설정 클릭**
    
    ![](/Images/2022/12/20/JDK_Install/Untitled%203.png)
#    
- **환경 변수(N)… 클릭**
    
    ![](/Images/2022/12/20/JDK_Install/Untitled%204.png)
#    
- **사용자 변수가 아닌 시스템 변수에서 새로 만들기 클릭**
    
    ![](/Images/2022/12/20/JDK_Install/Untitled%205.png)
    
    - **변수 이름(N)은 JAVA_HOME**
    - **변수 값(V)은 JDK파일을 압축 풀기하고 연 폴더 경로**
    (글쓴이는 D:\AI_Class\tools\jdk-17.0.4.1의 위치에 있음)
#    
- **모두 입력 후 확인**
    
    ![](/Images/2022/12/20/JDK_Install/Untitled%206.png)
#    
- **JAVA_HOME있는지 확인 / Path 클릭 후 편집 클릭**
    
    ![](/Images/2022/12/20/JDK_Install/Untitled%207.png)
#    
- **새로 만들기 클릭 -> D:\AI_Class\tools\jdk-17.0.4.1\bin 나 %JAVA_HOME%\bin 중 하나를 쓰시면 됩니다.**
    
    ![](/Images/2022/12/20/JDK_Install/Untitled%208.png)
    - **이후 확인 누르며 빠져나오기**
#
- **전부 확인을 눌러 설정 완료**
    
    ![](/Images/2022/12/20/JDK_Install/Untitled%209.png)
    

## 참고 (CLASS PATH)

- **Class Path**는 Java Application이 사용하고 있는 **Class가 여러 경로로 분산 되어 있을 때 하나로 모으기 위해 사용하는 방법**
#
- **새로 만들기 클릭**
    
    ![](/Images/2022/12/20/JDK_Install/Untitled%2010.png)
#    
- **CLASSPATH와 %JAVA_HOME%\lib 입력 후 확인**

    ![](/Images/2022/12/20/JDK_Install/Untitled%2011.png)

# 설치 확인

- **시작메뉴 옆에서 cmd 입력 후 명령 프롬프트 실행**
    
    ![](/Images/2022/12/20/JDK_Install/Untitled%2012.png)
#    
- **java -version 과 javac -version으로 확인**
    
    ![](/Images/2022/12/20/JDK_Install/Untitled%2013.png)
    
    - **다음과 같이 나오면 설치 완료**
        - **java -version에서 오류가 나올 시**에는 **Eclipse가 제대로 설치가 되어있는지 확인**
        - **javac -version에서 오류가 나올 시**에는 **환경 변수 설정이 잘못되어 있을 가능 성이 높아 환경 변수 설정 확인**