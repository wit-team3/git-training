# git-training

## 사용규칙

### 한번하는 작업

1. 이 저장소를 fork
2. git clone <fork된 내 github repo주소>
3. git remote add upstream <공용 원격 저장소 주소>  
   예를 들어, wit-team3의 git-training 주소
4. 다음을 입력하여 origin과 upstream을 확인합니다.

```git
git remote -v
```

- origin : 공용 repo를 내 계정에 fork한 repo
- upstream : 공용 repo

### 매번하는 작업

- 나의 작업 상태 수시로 확인하기

```git
git status
```

- 작업 브랜치 만들기

```git
git switch -c <브랜치 이름> origin/main
```

브랜치 이름은 작업한 내용을 표현합니다.

- commit 작성

```git
git add .
```

```git
git commit
```

커밋 작성후 esc를 누르고 :wq를 하여 저장합니다.

- 원격 저장소에 작업한 브랜치를 올리기

```git
git push origin <브랜치 이름>
```

- pull request 하기  
   ![image](https://user-images.githubusercontent.com/58525009/116854307-73701680-ac32-11eb-8a97-38125662837b.png)  
   fork된 내 repo에서 Compare & request를 누릅니다.

  ![image](https://user-images.githubusercontent.com/58525009/116854310-7539da00-ac32-11eb-8af1-63f0372f44b7.png)  
  내용을 작성하고 Create pull request를 누릅니다.

- merge하기전에 체크사항

1. 여러 개의 커밋 메시지를 하나로 통합합니다.  
   3개의 커밋 메시지를 통합하는 경우를 예시로 듭니다.

```git
git rebase -i HEAD~3
```

2. 최신상태를 반영합니다.

```git
git rebase origin/main
```

- merge하기  
  ![image](https://user-images.githubusercontent.com/58525009/116854315-7834ca80-ac32-11eb-855e-97c0408ea488.png)  
  Merge pull request를 누릅니다.

## 주의사항

1. fork한 저장소에서 작업하기
2. 원본 저장소에 commit, push하지 않기
3. 다른 팀원의 코드 merge하지 말기
