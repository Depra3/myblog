---
title: Git & Github 연결 설정
date: 2022/12/19 14:04:25
categories:
- R
- Baseball
tags:
- R
- Fight
- Shocking
---

# Git & Github 연결 설정

## 다운로드

- Git : [https://git-scm.com/downloads](https://git-scm.com/downloads)

![Untitled](/Images/2022/12/test/Untitled.png)

![Untitled](/Images/2022/12/test/Untitled%201.png)

- 설치 후 실행. (Default)
- 바탕화면에서 마우스 우클릭 후 Git Bash here 클릭

## 연결 설정

![Untitled](/Images/2022/12/test/Untitled%202.png)

- 연결에 문제가 있을 경우 연결을 끊고 다시 재연결 시도
- 바탕화면에 생긴 파일 위에 우클릭

![Untitled](/Images/2022/12/test/Untitled%203.png)

- Visual Studio Code 로 실행(단, 환경변수가 설정되어야함)

![Untitled](/Images/2022/12/test/Untitled%204.png)

- 없는 경우 설치시 PATH에 추가 CHECK

![Untitled](/Images/2022/12/test/Untitled%205.png)

- 있는 지 확인

![Untitled](/Images/2022/12/test/Untitled%206.png)

- 해당 사이트([https://www.toptal.com/developers/gitignore](https://www.toptal.com/developers/gitignore))에서 Python과 R 쓰고 생성

![Untitled](/Images/2022/12/test/Untitled%207.png)

- 나온 텍스트 내용을 복사

![Untitled](/Images/2022/12/test/Untitled%208.png)

- VS Code에 붙여넣기(맨 아랫줄에 붙여넣기)

![Untitled](/Images/2022/12/test/Untitled%209.png)

- 터미널 생성 후 powershell이 아닌 git bash로 체크 후 git add .gitignore부터 입력

![Untitled](/Images/2022/12/test/Untitled%2010.png)

![Untitled](/Images/2022/12/test/Untitled%2011.png)

- 나오는 오류는 로그인이 되지 않아서 발생함. 따라서 로그인해야함.

![Untitled](/Images/2022/12/test/Untitled%2012.png)

- 첫 줄은 로그인 ID, 두번째 줄은 닉네임으로 연결
- git config —global [user.email](http://user.email) “연결할 해당 github 가입 Email”
- git config —global [user.name](http://user.name) “연결할 해당 github 닉네임”
- 마지막으로 git push ( 로컬(local branch)에서 원격 저장소(remot repository)로
    
    보낼 때 사용하는 명령어) 로 마무리
    

![Untitled](/Images/2022/12/test/Untitled%2013.png)

- 나오는 사이트에서 Authorize 클릭

![Untitled](/Images/2022/12/test/Untitled%2014.png)

- 연결 완료 된 것 확인

![Untitled](/Images/2022/12/test/Untitled%2015.png)

![Untitled](/Images/2022/12/test/Untitled%2016.png)

- git add .
- git commit -m “updated” ※ update부분은 git commit message의 내용
- git push
- 위 코드를 이어 입력하여 업로드

![Untitled](/Images/2022/12/test/Untitled%2017.png)

![Untitled](/Images/2022/12/test/Untitled%2018.png)

- 변경이 되었는지 확인

# File과 Repository를 같은 이름으로 하여 연결 방법

- File명과 Repository를 같은 이름으로 한 후 File을 우클릭하여 Git Bash Here 실행 후 아래 부분의 코드를 한 줄 씩 입력

![Untitled](/Images/2022/12/test/Untitled%2019.png)