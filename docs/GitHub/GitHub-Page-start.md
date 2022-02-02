---
layout: default
title: GitHub Page 시작하기
parent: GitHub
nav_order: 1
---

# Typography
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}
---
https://zeddios.tistory.com/1222
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
확인 https://bysandychoi.github.io

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
git push

---
