# Codex와 협업하는 개발 워크플로

Codex를 단순한 코드 생성기가 아니라, 로컬 개발과 리뷰, 자동화, 운영까지 함께 설계하는 협업형 코딩 에이전트로 다루기 위한 집필 저장소입니다.

이 저장소는 기존 위키독스형 프로젝트 구조를 참고해 `README.md`, `TOC.md`, `pages/`, `assets/`, `examples/`를 중심으로 구성했습니다.

## 이 책이 다루는 것

- Codex의 개념, 실행 방식, 모델 선택 기준
- 프롬프트 설계, 작업 분해, AGENTS.md 기반 협업 규칙
- 로컬 개발, 디버깅, 리팩터링, 테스트 보강
- IDE, App, Cloud, GitHub PR 리뷰 확장
- `codex exec`, MCP, Skills, Plugins, API 내장
- 비용, 보안, 거버넌스, 실전 프로젝트

## 예상 독자

- Codex를 처음 쓰지만 실무 생산성까지 연결하고 싶은 개발자
- 에이전트형 개발 도구를 팀 프로세스에 붙이려는 엔지니어링 리더
- 로컬 개발, 코드 리뷰, 자동화, 운영 관점까지 한 번에 정리하고 싶은 독자

## 저장소 구조

```text
codex-practical-guide/
├─ README.md
├─ TOC.md
├─ pages/
│  ├─ 01-understand-and-start/
│  ├─ 02-collaborate-with-codex/
│  ├─ 03-local-development-workflows/
│  ├─ 04-ide-app-cloud/
│  ├─ 05-extend-and-automate/
│  └─ 06-operations-security-projects/
├─ assets/
└─ examples/
```

## 집필 원칙

1. 각 장은 "개념 -> 왜 중요한가 -> 실무에서 언제 문제되는가 -> 어떻게 쓰는가" 흐름으로 작성합니다.
2. 장별 실습은 가능한 한 같은 샘플 저장소를 반복 활용합니다.
3. 모델명이나 UI처럼 변경이 잦은 항목은 제품 소개보다 선택 원리 중심으로 씁니다.
4. 각 장 끝에는 체크리스트, 실수 포인트, 실무 적용 팁을 남깁니다.

상세 목차는 [TOC.md](./TOC.md)에서 관리합니다.
