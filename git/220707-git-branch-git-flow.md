# 오늘 한 일

- git

  - Branch 분기점을 생성하여 독립적으로 코드를 변경할 수 있도록 도와준다.  
    `git branch`  
    `git branch newBranchName`  
    `git switch main`  
    `git merge newBranchName`  
    `git branch -D newBranchName`

  - Merge CONFLICT  
    작성 시키고 싶은 모습으로 새 commit을 만들어 준다.
  - branch upstream  
    `git push -u origin newBranchName`
  - 원격 저장소에서 로컬 저장소로 가져오고 싶을 때  
    `git pull origin main`
  - git flow  
    https://danielkummer.github.io/git-flow-cheatsheet/index.ko_KR.html  
    `git flow init` `git flow feature start ` `git flow feature finish `
  - 되돌리기  
    `git mv ` `git restore ` `git commit --amend`
  - 잘못한 이력도 commit으로 박제하고 수정한 이력을 남기자!  
    `git revert --no-commit HEAD~n..` commit n개 전으로 돌아가겠습니다.

# 오늘의 코드

파일 이름 바꾸기 mv와 git mv의 차이: mv 의 경우, history 추적이 불가능해진다.

```
mv - deleted, new file
git mv - renamed
```

# 내일 할 일

- 필수 강의 ch. 9까지 (JS 선행)
- git 강의 -> 정리
- html/css 강의 복습

