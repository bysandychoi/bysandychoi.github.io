---
layout: default
title: GitHub Token
parent: GitHub
nav_order: 3
---

# GitHub Token
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}
---
[참조1 link]()

---

## GitHub token 저장하기 
코드가 있는 local 폴더에서 .git 의 config파일을 열어서 다음과 같이 수정  
숨은 파일 보이게 하는 단축 키 : command + shift + .
```
[remote "origin"] 부분의 url을
url = https://<user-id>:<token>@github.com/~/~.git
```

