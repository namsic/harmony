## Introduction
Harmony project에 기여하고자 하는 분들을 위한 참고 자료입니다. 각 하위 저장소에 따라 다른 규칙을 적용하는 경우도 있으니 참고 바랍니다.

## Github flow
본 프로젝트는 GitHub flow를 기반으로 개발을 진행하고 있습니다.
따라서 아래와 같은 흐름을 따르게 됩니다.
1. main branch는 항상 배포 가능한 상태를 유지
1. 변경이 필요한 경우 main branch에서 새 branch를 만들어 작업
1. Pull request를 생성하고 review 진행
1. review가 충분히 이루어진 후 merge
1. 작업하던 branch 삭제

Github flow에 대한 자세한 내용은 [Github Docs](https://docs.github.com/en/get-started/quickstart/github-flow)를 참고 바랍니다.

## Commit message
main branch의 commit message는 아래와 같은 형태를 가집니다.
여러 commit을 squash merge 하려는 경우 개별 commit은 merge 후 이력에 남지 않으므로 message를 자유롭게 작성해도 됩니다.
```
<type>: <subject>(<#PR_number>)

<body>

<footer>
```
- 첫 줄은 50자가 넘지 않도록 합니다.
  + type은 하단의 표를 참고 바랍니다.
  + subject는 명령문 형태로 작성합니다.
  + subject는 대문자로 시작하며, 마침표는 생략합니다.
- Body는 한 line에 72자 이내로 작성합니다.
  + 어떻게 변경했는지보다는 무엇을 왜 변경했는지 작성합니다.
- Footer에는 관련 issue, pull request 또는 공동 작업자를 작성합니다.
  + 대부분의 경우 pull request에서 관련 issue를 참조하므로 개별 commit message에 작성할 필요는 없습니다.

type | description
-- | --
feat | 기능 추가
fix | 버그 및 문제 수정
docs | 문서 관련 수정
style | code style, format 관련 수정
refactor | 기능 변화 없는 수정 또는 최적화
test | 테스트 관련 수정

## Issue
해야 할 작업, 논의가 필요한 내용 등 다양한 내용을 Issue로 작성합니다.
Issue를 이용하는 이유는 아래와 같습니다.
- 작업을 구체적으로 정리하고 검토
- 예정된 작업을 팀원과 공유 및 할당
- 작업 및 논의 과정을 기록으로 남겨 이후에 참고하기 위함

## Document
가능하면 주석을 많이 작성하거나 문서를 별도로 관리하기보다, 코드를 간결하게 작성하도록 합니다.
문서화 주석에 대한 가이드라인(Javadoc, python docstring 등)이 있는 경우 이를 따르도록 합니다.