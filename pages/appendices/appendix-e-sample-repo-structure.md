이 책의 실습은 한 번 쓰고 버리는 예제가 아니라, 여러 장에서 반복해서 재사용할 수 있는 샘플 저장소를 전제로 합니다.

## 목차

- 권장 구조
- 왜 이런 구조가 좋은가
- 이 구조로 실습할 수 있는 주제

## 권장 구조

```text
sample-project/
├─ README.md
├─ AGENTS.md
├─ backend/
│  ├─ app/
│  ├─ tests/
│  └─ requirements.txt
├─ frontend/
│  ├─ src/
│  ├─ tests/
│  └─ package.json
├─ docs/
├─ scripts/
└─ .github/
   └─ workflows/
```

## 왜 이런 구조가 좋은가

- `README.md`: 프로젝트 목적과 실행 방법을 설명하는 기준 문서
- `AGENTS.md`: Codex와 사람이 함께 지켜야 할 작업 규칙
- `backend/`, `frontend/`: 서로 다른 실행 환경과 테스트 방식을 가진 실습 대상
- `docs/`: 문서화 실습과 자동화 결과를 담는 공간
- `scripts/`: 반복 작업 자동화 예시
- `.github/workflows/`: CI/CD와 리뷰 자동화 실습 대상

## 이 구조로 실습할 수 있는 주제

- 코드베이스 탐색과 진입점 찾기
- 작은 기능 추가와 테스트 보강
- 버그 수정과 회귀 테스트 추가
- README와 운영 문서 업데이트
- CI/CD와 PR 리뷰 자동화
- `AGENTS.md`와 설정 파일 적용

핵심은 실습 저장소가 너무 깨끗하지도, 너무 복잡하지도 않아야 한다는 점입니다. 약간의 거친 부분과 개선 포인트가 있어야 Codex의 활용 장면이 자연스럽게 드러납니다.
