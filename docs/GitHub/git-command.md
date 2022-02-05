---
layout: default
title: Git 명령어 정리
parent: GitHub
nav_order: 5
---
[Git official document](https://git-scm.com/docs/git)
- console END : q

# Git 명령어 정리

## Option
- `__--version__`    
  Prints the Git suite version that the git program came from.

## add
- `git add <filepath>, git add .`    
  Add file contents to the index

## branch
- `git branch <newbranch>`       
  create branch
- `git branch -r`    
  List the remote-tracking branches
- `git branch -a`     
  List both remote-tracking branches and local branches     
- `git branch -m <oldebranch> <newbranch>`   
  change branch name
- `git branch -d <branchname>`   
  delete branch

## checkout
- `git checkout <branchname>`   
  Updates files in the working tree to match the version in the index or the specified tree.
- `git checkout -t <remotepath>/<branchname>`       
  remote branch

## commit
- `git commit -m "<commit_description>"`  
  commit (in local), Record changes to the repository

## fetch
- `git fetch`  
  Download objects and refs from another repository

## pull
- `git pull`  
  Fetch from and integrate with another repository or a local branch

## init
- `git init`     
  Create an empty Git repository  
  
## log  
- `git log`    
  Show commit logs

## clone
- `git clone <gitpath>`      
  Clone a repository into a new directory

## push
- `git push <remote_name> <branchname>`  
  Update remote refs along with associated objects
- `git push <remote_nmae>--delete <branch_name>`  
  delete remote branch

## show 
Show various types of objects
- `git show <commit_ID>`  
  특정 commit 내역 확인
 
## reset
- `git reset -- hard HEAD^`   
  commit 한 이전 코드 취소
- `git reset -- soft HEAD^`     
  코드는 살리고 commit만 취소 
- `git reset -- hard HEAD && git pull`    
  git 코드 강제로 모두 받아오기                 

## config
- `git config --global user.name "<username>"`  
  git account name
- `git config --global user.name "<useremail>"`  
  git account email
- `git config --list` 
