---
title: "Making a Weg Page using Hugo in R"
subtitle: "Web Page Making with Hugo in R"
author: 권세훈(상명대)
tags:
  - WSL
  - R
  - Hugo
  - Git
output: 
  html_document:
    toc: true
    toc_float:
      toc_collapsed: true
    toc_depth: 5
    number_sections: true
    theme: lumen
---

# Web Page Making with Hugo in R

# Prepare 기본 구조 준비 

- [RStudio](https://www.rstudio.com/) : 개인 작업 담당 
- [GitHub](https://github.com/) : 버전 컨츠롤(for the code version control) 
- [Netlify](https://www.netlify.com/) : 웹페이지 게시(for the web publish) 

# GitHub

- Create a new repository : naming the project <br/> 
  저장소 개설 및 프로젝트명 설정 

  * Public/Private 선택
  * Initialize 초기 설정 
    - README.md 
    - .gitignore: ex. R 
    - license: ex. MIT

- copy the repository URL or SSH <br/> 
  저장소 주소를 복사

# RStudio

## Create a New Project 새로운 프로젝트 만들기 

- Version Control 
- Git 
- URL/Name/Directory 

## Hugo package 패키지 설치 및 실행

### install Package

```
install.packages("blogdown")
blogdown::install_hugo()
```
  * Check the Hugo version  
  미리 버전을 확인하자 
  * Later, you can check the version by command `Hugo_version()` 

### Create Website 

```
blogdown::new_site(theme="h-enk/doks", force = TRUE)
```
- [Hugo theme](https://gohugo.io/) 싸이트에서 다른 테마도 이용 가능
- You can use other themes in [Hugo theme](https://gohugo.io/) 

### 로컬 환경에서 웨페이지 미리 보기

```
blogdown::serve_site()
```
- RStudido 에서 임시로 웹서버 기능을 실행해 웹페이지 내용을 미리 볼 수 있다

## RStudio 에서 깃 명령 실행

### 깃 명령은 3단계로 구성 

- Git requires three steps

  1) add
  2) commit
  3) push

- Rstudio Git menu provide these three steps <br/> 
  Rstudio 에서도 Git 방식으로 프로젝트 만들면 Git 메뉴가 생김
  
  1) add: click the selection boxes for the files/directories
  2) commit: writing commit message and click the commit button
  3) push: click the push button to upload the files to the GitHub 

- You can also do the same jobs in your own command line terminal <br/>
  한편 Rstudio와 별개로 명령창에서도 깃 명령 직접 실행 가능 
  * 자세한 사항은 [Git Guide 참고](/content/posts/Git_guide.html)
  
### 짜잔

앞에서 푸쉬 명령으로 GitHub에 프로젝트를 올리면 <br/>
바로 Netlify 웹페이지가 생성/수정됨!!!


# 문서 내용 전반의 기본 출처

- https://samtoet.cool/posts/how-tf-does-this-blog-thing-work/ 
- https://aispiration.com/comp_document/ds-netlify-protection.html#

---
End of Doc