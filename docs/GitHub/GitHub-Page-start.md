---
layout: default
title: GitHub Page 시작하기
parent: GitHub
nav_order: 1
---

# GitHub Page 시작하기
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}
---
[참조1 link](https://zeddios.tistory.com/1222)

---

## GitHub page 용 GitHub Repository 생성

새로운 Repository 생성 
반드시 username.github.io 식으로 생성

GitHub repository clone 하기 
```
git clone 복사한 주소 
```
clone 한 폴더로 이동한 다음 파일 생성
```
cd username.github.io 
echo "Hello World" > index.html
```
push
```
git add --all 
git commit -m "Initial commit" 
git push -u origin main
```
확인 
[https://bysandychoi.github.io](https://bysandychoi.github.io)

---
## Jekyll 설치
정적 사이트 생성기 
```
gem install jekyll bundler
```
기존 생성한 index.html제거 후
아까 클론한 내 github.io 폴더!! 그 경로로 이동해서 위 명령어 실행 
```
jekyll new ./
```
bundle install
```
bundle install
```
Jekyll을 로컬서버에 띄우기
```
bundle exec jekyll serve
```
![img]({{"/assets/images/jekyll-serve.png"| relative_url}})

원격에 git push
```
git add . 
git commit -m "본인의 커밋 메세지" 
git push
```
---
## 테마 선택
 아래에서 사용하고자 하는 테마 선택
 - [jamstackthemes.dev](https://jamstackthemes.dev/ssg/jekyll/)
 - [jekyllthemes.org](http://jekyllthemes.org/)
 - [jekyllthemes.io](https://jekyllthemes.io/)
 - [jekyll-themes.com](https://jekyll-themes.com/)

---
## 테마 적용
선택한 테마 링크로 이동  
[just-the-docs](https://github.com/pmarsceill/just-the-docs)  

우측의 code를 클릭 후 download zip 클릭  
![img]({{"/assets/images/download-theme.png"| relative_url}})  
다운받은 폴더 열어 전체 복사 후 내 github.io 폴더에 붙혀넣기, 모두 대치로 붙이기 

터미널에 bundle install 입력 (sudo 붙이고 실행하기)
```
bundle install
```  
serve 재 가동 (sudo 붙이고 실행하기)
```
bundle exec jekyll serve
```  

원격에 push
```
git add . 
git commit -m "본인의 커밋 메세지" 
git push
```
