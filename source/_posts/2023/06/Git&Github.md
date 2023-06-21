---
title: Git & Github 연결 설정
date: 2023/06/21 21:00:00
categories:
- Utile
tags:
- Git
- Github
---

## ☆ 다운로드 링크 ☆

### [Git Downloads](https://git-scm.com/downloads)

- 사용자가 사용하는 OS(운영체제) 선택하여 다운로드 합니다.
    ( 글쓴이는 Windows 10이므로 Windows 선택 )
    
    ![](/Images/2023/06/Git&Github/Untitled.png)
    
- 사용자가 사용하는 OS bit를 선택하여 다운로드 합니다. ( 글쓴이는 64bit이므로 64bit 선택 )
    
    ![](/Images/2023/06/Git&Github/Untitled%201.png)
    
- 설치 후 실행. (Default)
- 바탕화면에서 마우스 오른쪽 클릭 후 Git Bash here 클릭
    - git —version입력하여 설치 확인

- **① code** 클릭 → **②** 클릭
    - git clone “링크”
    
    ![](/Images/2023/06/Git&Github/Untitled%202.png)
    
- 바탕화면에 생긴 파일 위에 오른쪽 클릭
    
    ![](/Images/2023/06/Git&Github/Untitled%203.png)
    
- Visual Studio Code 로 실행(단, 환경변수가 설정되어야함)
    - 참고 : [Visual Studio Code 설치 및 환경 설정](https://depra3.github.io/2023/06/18/2023/06/18/Visual_Studio_Code_Install/)
        
    ![](/Images/2023/06/Git&Github/Untitled%204.png)
    
- 해당 사이트([https://www.toptal.com/developers/gitignore](https://www.toptal.com/developers/gitignore))에서 사용하는 언어 입력]
    - ex) Python, R
    
    ![](/Images/2023/06/Git&Github/Untitled%206.png)
    
- 나온 텍스트 내용을 복사
    
    ![](/Images/2023/06/Git&Github/Untitled%207.png)
    
- VS Code에서 .gitignore에 붙여넣기(맨 아랫줄에 붙여넣기)
    
    ![](/Images/2023/06/Git&Github/Untitled%208.png)
    
- 터미널 생성 후 powershell이 아닌 git bash로 체크 후 git add .gitignore 입력
    
    ![](/Images/2023/06/Git&Github/Untitled%209.png)
    
    ![](/Images/2023/06/Git&Github/Untitled%2010.png)
    
- 나오는 오류는 로그인이 되지 않아서 발생함. 따라서 로그인해야함.
    
    ![](/Images/2023/06/Git&Github/Untitled%2011.png)
    
- 첫 줄은 로그인 ID, 두번째 줄은 닉네임으로 연결
- git config —global [user.email](http://user.email) “연결할 해당 github 가입 Email”
- git config —global [user.name](http://user.name) “연결할 해당 github 닉네임”
- 마지막으로 git push ( 로컬(local branch)에서 원격 저장소(remot repository)로
    
    보낼 때 사용하는 명령어) 로 마무리
    
    ![](/Images/2023/06/Git&Github/Untitled%2012.png)
    
- 나오는 사이트에서 Authorize 클릭
    
    ![](/Images/2023/06/Git&Github/Untitled%2013.png)
    
- 연결 완료 된 것 확인
    
    ![](/Images/2023/06/Git&Github/Untitled%2014.png)
    
- 아래 코드를 입력하여 업로드
    - git add .
    - git commit -m “updated” ※ update부분은 git commit message의 내용
    - git push
    
    ![](/Images/2023/06/Git&Github/Untitled%2015.png)
    
- 변경이 되었는지 확인
    
    ![](/Images/2023/06/Git&Github/Untitled%2016.png)
    
    ![](/Images/2023/06/Git&Github/Untitled%2017.png)
    

# File과 Repository를 같은 이름으로 하는 연결 방법

- File명과 Repository를 같은 이름으로 한 후 File을 우클릭하여 Git Bash Here 실행 후 아래 부분의 코드를 한 줄 씩 입력
    
    ![](/Images/2023/06/Git&Github/Untitled%2018.png)