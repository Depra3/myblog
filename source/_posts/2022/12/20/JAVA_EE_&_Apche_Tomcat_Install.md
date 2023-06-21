---
title: JAVA EE & Apche Tomcat 설치
date: 2022/12/27 18:00:00
categories:
- JAVA
tags:
- JAVA EE
- JDK
- Apache Tomcat
---

# JAVA EE를 사용하기 위한 Eclipse 다운로드

## ★ 다운로드 링크 ★

[Eclipse Packages | The Eclipse Foundation - home to a global community, the Eclipse IDE, Jakarta EE and over 350 open source projects...](https://www.eclipse.org/downloads/packages/)

- 아래의 그림에서 이용자의 운영체제에 맞게 선택하여 다운로드
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled.png)
    
- 어느 것을 선택하든 같은 것을 다운 받기 때문에 신경 쓰지 않고 다운로드
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%201.png)
    

# JDK 설치

## [★ JDK 설치 및 환경 변수 설정 링크 ★](https://depra3.github.io/2022/12/19/2022/12/20/JDK_Install/)

# Apache Tomct 다운로드

## ★ 다운로드 링크 ★

[Apache Tomcat®](https://tomcat.apache.org/download-90.cgi)

- 원하는 버전 선택 ( **글쓴이는 배운 환경과 같은 Tomcat 9를 이용** )
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%202.png)
    
- **zip** **클릭**해서 다운로드
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%203.png)
    

- 다운로드 한 폴더에 그대로 압축 풀기
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%204.png)
    
- eclipse 실행
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%205.png)
    
- 원하는 경로로 설정하고 싶으면 **①** **Browse** 클릭
- 기본 경로로 만들어서 사용한다면 그대로 **② Launch** 클릭
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%206.png)
    
    - **※** **①** **Browse** 클릭했을 경우 원하는 경로 선택 후 **폴더 선택** 클릭
        
        ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%207.png)
        
    
- 경로가 바뀐 것을 볼 수 있다.
- **Launch** 클릭하여 Eclipse 실행
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%208.png)
    
- 아래 그림과 같이 나왔다가 실행이 된다.
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%209.png)
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2010.png)
    

## 작업하기 위한 기본 설정

### 요약

- **Web > CSS Files > Encoding : ISO 10646/Unicode(UTF-8)** 선택
- **Web > HTML Files > Encoding : ISO 10646/Unicode(UTF-8)** 선택
- **Web > JSP Files > Encoding : ISO 10646/Unicode(UTF-8)** 선택
- **Server > Runtime Environments > Add > Apache > Apache 버전** 선택 **> Next > Browse >**
    
    압축 해제한 **Apache Tomcat 폴더** 클릭 > **폴더 선택** 클릭 > **Finish** 클릭 > 추가되었는지 확인 >
    
    **Apply and Close** 클릭
    

### 상세

- 상단의 **Window** - **Preferences** 클릭
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2011.png)
    
- **①** Web 좌측의 ‘**>’** 클릭 → **②** CSS Files 좌측의 ‘**>**’ 클릭 → **③** **Korean, EUC-KR** 클릭 →
    
    **④** **ISO 10646/Unicode(UTF-8)**을 찾아 클릭 ( 스크롤을 맨 위에 올리면 있음 )
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2012.png)
    
- **①** **Apply** 클릭하여 적용 **→ ②** **HTML Files** 클릭
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2013.png)
    
- **①** **Korean, EUC-KR** 클릭 **→ ②** **ISO 10646/Unicode(UTF-8)**을 찾아 클릭 ( 위와 위치 동일함 )
    
    **→ ③** **Apply** 클릭하여 적용 **→ ④ JSP Files** 클릭
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2014.png)
    
- **①** **Korean, EUC-KR** 클릭 **→ ②** **ISO 10646/Unicode(UTF-8)**을 찾아 클릭 ( 위와 위치 동일함 )
    
    **→ ③** **Apply** 클릭
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2015.png)
    
- **① Server** 좌측의 ‘**>**’ 클릭 **→** **② Runtime Environments** 클릭 **→ ③ Add..** 클릭
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2016.png)
    
- **① Apache** 좌측의 ‘**>**’ 클릭 → **②** 자신이 받은 Apache Tomcat 버전에 맞게 클릭 →
    
    **③** ‘**②**’를 진행하면 비활성화 되어 있는 **Next** 버튼이 활성화 되니 **Next** 클릭
    
- 글쓴이는 Apache Tomcat 9를 다운 받음
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2017.png)
    
- **① Browse..** 클릭 → 폴더 선택 창이 나옴 → **②** 압축 해제한 **Apache Tomcat 폴더** 클릭 →
    
    **③ 폴더 선택** 클릭 → **④** 활성화 된 **Finish** 클릭
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2018.png)
    
- 추가 되었는지 확인 후 **① Apply and Close** 클릭
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2019.png)
    

# Test

- **① Create a Dynamic Web project** 클릭 → **② Project name**에 원하는 이름 쓰기 →
    
    **③ Finish** 클릭
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2020.png)
    
- **① webapp**에서 마우스 **오른쪽** 클릭 → **② New**에 마우스 커서를 놓기 →
    
    **HTML File**이 있다면 클릭 / 없다면 **Other..** 클릭
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2021.png)
    
- **※** **Other..** 클릭 후
    
    **① html** 입력하면 **② HTML File** 이 자동으로 나옴 → **③ Next** 클릭
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2022.png)
    
- **① Test.html** 입력 → **② Next** 클릭
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2023.png)
    
- **Finish** 클릭
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2024.png)
    
- 예시로 “연동 확인 !!” 입력
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2025.png)
    
- **① Test.html** 마우스 오른쪽 클릭 → **② Run As**에 마우스 커서 놓기 → **③ Run on Server** 클릭
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2026.png)
    
- **①** 자신이 설치한 Tomcat 버전 클릭 (**글쓴이는 Tomcat 9 설치**) → **② Next** 클릭
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2027.png)
    
- Project Name인 **Test**있는지 확인 → **Finish** 클릭
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2028.png)
    
- **연동 성공!**
    
    ![](/Images/2022/12/20/JAVA_EE_&_Apche_Tomcat_Install/Untitled%2029.png)