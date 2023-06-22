---
title: Node.js - Github Blog
date: 2023/06/22 22:00:00
categories:
- Utile
tags:
- Git
- Github
- Node.js
---

## ★ 다운로드 링크 ★

- [Nodejs.org](https://nodejs.org/en)에서 설치
    /Images/2023/06/Node.js-Github_Blog
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled.png)
    
- Add to PATH가 있는 지 확인
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%201.png)
    
- 빨간 박스 체크
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%202.png)
    
- 흐름대로 가면 아래와 같이 설치 완료
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%203.png)
    
- 바탕 화면 - Git Bash Here
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%204.png)
    
- 아래와 같이 순서대로 진행 - 이후 localhost:4000이 되는지 확인
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%205.png)
    
    - npm install -g hexo-cli
    - hexo init myblog(파일명)
    - cd myblog/
    - hexo server

- 편의를 위해 VS Code이용하기 위해 아래와 같이 진행
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%206.png)
    
- Git Bash 창에서 code .입력
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%207.png)
    
- _config.yml 파일에서 사용할 url 입력
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%208.png)
    

- Github에서 Repository 생성
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%209.png)
    

- _config.yml 파일에서 deploy 내용 입력
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%2010.png)
    

- 터미널 열기
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%2011.png)
    

- Git Bash로 접속
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%2012.png)
    

- 아래의 내용 순서대로 입력
    - npm install
    - npm install hexo-server —save
    - npm install hexo-deployer-git —save
    - hexo generate
    - hexo deploy
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%2013.png)
    

# 백업

- 폴더명과 Repository name과 항상 같아야함 / 배포 X 백업 O

![](/Images/2023/06/Node.js-Github_Blog/Untitled%2014.png)

- 차례대로 입력하거나 한번에 입력하여 연동
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%2015.png)
    
- 파일 백업
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%2016.png)
    
- 화면 관리 - [https://hexo.io/ko/docs/front-matter](https://hexo.io/ko/docs/front-matter)
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%2017.png)
    

# 블로그 게시글 올리기

- 편하게 Notion을 이용해 올리는 방법

![](/Images/2023/06/Node.js-Github_Blog/Untitled%2018.png)

![](/Images/2023/06/Node.js-Github_Blog/Untitled%2019.png)

- 다운 받은 파일 압축 풀기
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%2020.png)
    

- VS Code에서 이미지 경로 입력
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%2021.png)
    

- Github에 올리기
    - git add .
    - git commit -m “updated”
    - git push
- Github 블로그에 배포하기
    - hexo generate
    - hexo deploy  (배포)
    - hexo server
    
    ![](/Images/2023/06/Node.js-Github_Blog/Untitled%2022.png)