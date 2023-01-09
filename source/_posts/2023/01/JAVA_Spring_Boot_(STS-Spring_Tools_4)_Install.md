---
title: JAVA Spring Boot(STS - Spring Tools 4) 설치
date: 2023/01/07 18:00:00
categories:
- JAVA
tags:
- JAVA EE
- JDK
- JAVA Spring
---

# JAVA Spring Boot를 사용하기 위한 준비

- **Eclipse EE version은 2022-09(4.25.0)**
- **설치 방법 링크**
    
    [JAVA EE & Apche Tomcat 설치](https://depra3.github.io/2022/12/27/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/)

- **Help** → **Eclipse Marketplace…** 클릭 (잠시 동안 로딩이 있을 수 있습니다.)
    
    ![Untitled](/Images/2023/01/JAVA_Spring_Boot_(STS-Spring_Tools_4)_Install/Untitled.png)
    
- **sts** 검색 → 최신 버전(현재는 Spring Tools 4가 최신) 찾기 → **Install** 클릭
    
    ![Untitled](/Images/2023/01/JAVA_Spring_Boot_(STS-Spring_Tools_4)_Install/Untitled%201.png)
    
- **Confirm** 클릭
    
    ![Untitled](/Images/2023/01/JAVA_Spring_Boot_(STS-Spring_Tools_4)_Install/Untitled%202.png)
    
- 약 2~3분 정도 소요됩니다.
    
    ![Untitled](/Images/2023/01/JAVA_Spring_Boot_(STS-Spring_Tools_4)_Install/Untitled%203.png)
    
- **①** **동그라미** 체크 → **② Finish** 클릭
    
    ![Untitled](/Images/2023/01/JAVA_Spring_Boot_(STS-Spring_Tools_4)_Install/Untitled%204.png)
    
- 붉은 박스 클릭하면 현재 진행도가 상세하게 나옵니다.
- 설치에 시간이 걸리니 커피 한 잔을 타고 와서 지켜봅시다.(약 4분 정도 소요됨)
    
    ![Untitled](/Images/2023/01/JAVA_Spring_Boot_(STS-Spring_Tools_4)_Install/Untitled%205.png)
    
- 설치 중간에 갑자기 Trust 창이 뜹니다.
- **① Select All** 클릭 → **② Trust Selected** 클릭
    
    ![Untitled](/Images/2023/01/JAVA_Spring_Boot_(STS-Spring_Tools_4)_Install/Untitled%206.png)
    
- **Restart Now** 클릭
    
    ![Untitled](/Images/2023/01/JAVA_Spring_Boot_(STS-Spring_Tools_4)_Install/Untitled%207.png)
    
- Eclipse가 다시 시작되니 한 잔 타 온 커피를 마시면서 기다려봅시다.
    
    ![Untitled](/Images/2023/01/JAVA_Spring_Boot_(STS-Spring_Tools_4)_Install/Untitled%208.png)
    

## ☆ TEST ☆

- **File** 클릭 → **New**에 마우스 커서 놓기 → **Other..** 클릭
    
    ![Untitled](/Images/2023/01/JAVA_Spring_Boot_(STS-Spring_Tools_4)_Install/Untitled%209.png)
    
- **① spring** 입력 (자동 검색) → **② Spring Starter Project** 클릭 → **③ Next** 클릭
    
    ![Untitled](/Images/2023/01/JAVA_Spring_Boot_(STS-Spring_Tools_4)_Install/Untitled%2010.png)
    
- **①** Project 이름 / **②** Gradle - Groovy로 설정 / **③** 클릭하여 8로 설정  / **④** 클릭하여 War로 설정
    
    (**글쓴이가 배운 설정입니다.**)
    
    ![Untitled](/Images/2023/01/JAVA_Spring_Boot_(STS-Spring_Tools_4)_Install/Untitled%2011.png)
    
- 설정 후 확인
    
    ![Untitled](/Images/2023/01/JAVA_Spring_Boot_(STS-Spring_Tools_4)_Install/Untitled%2012.png)
    
- **① spring web** 입력 → **②** 네모박스 체크 → **③** 선택되었는지 확인 → **④ Finish** 클릭
    
    ![Untitled](/Images/2023/01/JAVA_Spring_Boot_(STS-Spring_Tools_4)_Install/Untitled%2013.png)
    
- 그림과 같은 구조로 생성되는 것을 확인할 수 있습니다.
    
    ![Untitled](/Images/2023/01/JAVA_Spring_Boot_(STS-Spring_Tools_4)_Install/Untitled%2014.png)
    

- 간혹 유효성 관련한 창이 뜨기도 하는데 검색해보니 검색을 잘 못하는 건지 찾기가 힘듭니다.
    
    아무거나 클릭해도 무방할 듯 싶습니다.
    
    ![Untitled](/Images/2023/01/JAVA_Spring_Boot_(STS-Spring_Tools_4)_Install/Untitled%2015.png)