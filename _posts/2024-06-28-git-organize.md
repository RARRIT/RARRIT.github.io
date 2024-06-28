---
title: "[Git] 깃(Git) 사용법 및 용어정리"
date: 2024-06-28
layout: single
toc: true
toc_label: "목차"
toc_icon: "align-left"
toc_sticky: true
categories:
  - git
tags:
  - common
  - git
author_profile: true
sidebar_main: true
---

* TOC
{:toc}

## Git 사용법 및 용어 정리

### Git 사용법

1. **설치 및 설정**
    ```bash
    # Git 설치 (OS에 따라 다름)
    sudo apt-get install git       # Ubuntu
    brew install git               # macOS
    winget install --id Git.Git -e # Windows

    # 사용자 정보 설정
    git config --global user.name "Your Name"
    git config --global user.email "your.email@example.com"
    ```

2. **저장소 초기화**
    ```bash
    git init
    ```

3. **원격 저장소 연결**
    ```bash
    git remote add origin [원격 저장소 URL]
    ```

4. **파일 추가 및 커밋**
    ```bash
    git add [파일명]             # 파일 추가
    git add .                    # 모든 변경 파일 추가
    git commit -m "커밋 메시지"  # 커밋
    ```

5. **브랜치 생성 및 전환**
    ```bash
    git branch [브랜치명]       # 브랜치 생성
    git checkout [브랜치명]     # 브랜치 전환
    git checkout -b [브랜치명]  # 브랜치 생성 후 전환
    ```

6. **원격 저장소와의 동기화**
    ```bash
    git pull origin [브랜치명]  # 원격 저장소의 변경 내용 가져오기
    git push origin [브랜치명]  # 로컬 변경 내용 원격 저장소에 반영
    ```

7. **브랜치 병합**
    ```bash
    git checkout [기준 브랜치]  # 기준 브랜치로 전환
    git merge [병합할 브랜치]   # 병합
    ```

### 유용한 Git 명령어

- **로그 확인**: `git log`
- **상태 확인**: `git status`
- **파일 비교**: `git diff [파일명]`
- **Stash 적용**: `git stash apply`
- **Stash 목록 확인**: `git stash list`
- **Stash 삭제**: `git stash drop`
   

### Git의 용어 정리

1. **Repository (저장소)**: 프로젝트의 파일들과 변경 이력들을 저장하는 곳이며, 로컬 저장소와 원격 저장소로 나뉜다.
   - **로컬 저장소**: 자신의 컴퓨터에 저장된 저장소
   - **원격 저장소**: 네트워크 서버에 저장된 저장소 (예: GitHub, GitLab)

2. **Clone**: 원격 저장소의 전체 내용을 로컬 저장소로 복사한다. `git clone [URL]`

3. **Commit**: 파일의 변경 사항을 저장소에 기록한다. 각 커밋은 고유한 해시 값을 가지며, 변경 이력 추적에 사용됨. `git commit -m "메시지"`

4. **Branch (브랜치)**: 독립적으로 작업을 진행할 수 있는 가지를 의미한다. 기본 브랜치는 `main` 또는 `master` 이며, 새로운 기능 개발이나 버그 수정을 위해 브랜치를 생성한다. `git branch [브랜치명]`

5. **Merge**: 두 브랜치를 하나로 합치는 작업. `git merge [브랜치명]`

6. **Checkout**: 특정 브랜치나 커밋으로 작업 디렉토리를 전환한다. `git checkout [브랜치명/커밋 해시]`

7. **Pull**: 원격 저장소의 변경 내용을 로컬 저장소로 가져온다. `git pull`

8. **Push**: 로컬 저장소의 변경 내용을 원격 저장소로 업로드한다. `git push`

9. **Stash**: 현재 작업 중인 변경 사항을 임시로 저장하고, 작업 디렉토리를 깨끗하게 만든다. `git stash`

10. **Fetch**: 원격 저장소의 변경 사항을 로컬 저장소로 가져오지만, 로컬 작업 디렉토리에 적용하지는 않는다. `git fetch`

