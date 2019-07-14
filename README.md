# Git-flow

Git-flow전략을 세워 효율적인 Source 관리를 하기 위해 만든 Reopsitory

> 참고 링크 : 우아한 형제들 기술 블로그 ([링크](http://woowabros.github.io/experience/2017/10/30/baemin-mobile-git-branch-strategy.html))

## Git-flow Branches

### Branches

| Branch Name |       목적                 |
|:-----------:|:-------------------------:|
|master       |제품으로 출시될 수 있는 branch   |
|develop      |다음 출시 버전을 개발           |
|feature      |기능을 개발                   |
|release      |이번 출시 버전을 준비           |
|hotfix       |출시 버전에서 발생한 버그를 수정   |

### Git flow 설명 그림

![Git flow 설명 그림](./img/git-flow_overall_graph.png)


1. master branch
2. master branch에서 develop branch 추가됨
3. develop 브랜치에서 상시로 버그를 수정한 커밋들이 추가됨
4. 새로운 기능 추가 작업이 있을 경우 develop 브랜치에서 feature 브랜치 생성
5. feature branch는 develop branch에서 시작됨
6. 기능 추가 작업 완료시 develop branch에 merge됨
7. develop에 이번 버전에 포함되는 모든 기능이  merge 되었다면 QA를 하기 위해 develop 브랜치에서 release브랜치를 생성함
8. QA 진행하면서 발생한 버그들은 release 브랜치에 수정됨
9. QA를 무사히 통과했다면 release 브랜치를 master와 develop 브랜치로 merge 함
10. 마지막으로 출시된 master 브랜치에서 버전 태그를 추가함.

[주요 사항 링크 : A successful Git branching model](https://nvie.com/posts/a-successful-git-branching-model/)

