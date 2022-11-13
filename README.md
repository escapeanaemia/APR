# APR
Automate Pull Request is a series of actions which can automatically run for pull request open, close etc.


## Open Pull Request
[Open Pull Request](https://github.com/escapeanaemia/APR/actions/workflows/AOPR.yml) workflow dispatch 이벤트를 실행해서 PR을 자동으로 생성할 수 있습니다.

<img width="300" alt="스크린샷 2022-11-13 오후 9 47 37" src="https://user-images.githubusercontent.com/19788090/201522451-28b6cab4-b2ab-42c6-a6e1-500873413312.png">


PR을 생성하기 위해 본 예제에서는 아래의 과정을 따릅니다
1. 임의로 브랜치 생성 및 체크아웃
2. 생성된 브랜치의 변경사항을 남기기 위한 txt 파일 생성 및 커밋
3. `main` 브랜치로 머지하는 Pull Request 자동 생성
4. Pull Request 생성시 `automerge` 라벨 부여

*automerge 라벨을 부여하는 이유는 PR을 자동으로 Approve 하고 머지하기 위함입니다.


## Merge Pull Request
[Merge Pull Request](https://github.com/escapeanaemia/APR/blob/main/.github/workflows/AMPR.yml) 는 PR 생성시 automerge 라벨이 부여되어 있으면 자동으로 PR Approve & Merge를 진행합니다.
본 프로젝트는 main 브랜치에 branch protection이 적용되어 있으며 최소 1명 이상의 Approve를 받아야만 머지를 진행 할 수 있습니다.
