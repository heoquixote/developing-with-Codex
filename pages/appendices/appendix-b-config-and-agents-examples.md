# Appendix B. config.toml / AGENTS.md 예시 모음

이 Appendix는 개인 설정과 프로젝트 규칙을 어떻게 분리하면 좋은지 보여주는 실전 예시를 제공합니다.

## 목차

- 1. `config.toml` 예시
- 2. 저장소 루트 `AGENTS.md` 예시
- 목적
- 공통 규칙
- 코드 스타일
- 리뷰 기준
- 3. 디렉터리별 `AGENTS.md` 예시
- 4. 분리 원칙

## 1. `config.toml` 예시

```toml
model = "gpt-5.4"
reasoning_effort = "medium"
approval_policy = "on-request"
sandbox_mode = "workspace-write"

[profiles.fast]
model = "gpt-5.4-mini"
reasoning_effort = "low"

[profiles.deep]
model = "gpt-5.4"
reasoning_effort = "high"
approval_policy = "on-request"
```

### 해설

- 기본 프로필은 일상적인 탐색과 구현에 맞춥니다.
- `fast`는 빠른 왕복이 중요할 때 씁니다.
- `deep`는 설계 검토나 큰 변경처럼 생각 비용이 필요한 경우에 씁니다.

## 2. 저장소 루트 `AGENTS.md` 예시

```markdown
# AGENTS.md

## 목적
- 이 저장소는 Python API 서버와 React 프론트엔드로 구성된다.

## 공통 규칙
- 관련 없는 파일은 수정하지 않는다.
- 구현 후 테스트 또는 정적 검사를 실행한다.
- 공개 API 시그니처 변경은 명시적으로 보고한다.

## 코드 스타일
- Python은 작은 함수와 명확한 타입 힌트를 선호한다.
- React는 기존 폴더 구조와 네이밍을 따른다.
- 주석은 필요할 때만 추가한다.

## 리뷰 기준
- 버그 가능성
- 회귀 위험
- 테스트 누락
- 운영 영향
```

## 3. 디렉터리별 `AGENTS.md` 예시

```markdown
# frontend/AGENTS.md

- 디자인 시스템 컴포넌트를 우선 사용한다.
- 임의의 색상/spacing 값 하드코딩 금지
- 접근성 속성 누락 금지
```

```markdown
# backend/AGENTS.md

- DB 스키마 변경은 마이그레이션 파일과 함께 제출한다.
- 외부 API 호출은 timeout/retry 정책을 확인한다.
- 로깅에는 민감정보를 남기지 않는다.
```

## 4. 분리 원칙

- `config.toml`은 개인의 작업 방식과 실행 권한을 다룹니다.
- `AGENTS.md`는 저장소가 요구하는 규칙과 기대 결과를 다룹니다.
- 개인 취향은 `config.toml`로, 팀 규칙은 `AGENTS.md`로 두어야 충돌이 줄어듭니다.

같은 내용을 두 파일에 중복으로 적기 시작하면 관리 비용이 급격히 올라갑니다. 무엇이 개인 설정이고 무엇이 팀 표준인지 구분하는 것이 핵심입니다.
