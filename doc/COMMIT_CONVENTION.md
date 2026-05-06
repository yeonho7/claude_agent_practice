# Commit Convention

## 개요
이 문서는 이 프로젝트에서 따를 Commit Convention을 정의합니다.

## Commit Message 형식

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Type (필수)
commit의 종류를 명시합니다.

- **feat**: 새로운 기능 추가
- **fix**: 버그 수정
- **docs**: 문서 수정 (코드 변경 없음)
- **style**: 코드 스타일 변경 (포매팅, 세미콜론 등)
- **refactor**: 코드 리팩토링 (기능 변경 없음)
- **perf**: 성능 개선
- **test**: 테스트 추가 또는 수정
- **chore**: 빌드, 의존성 업데이트 등

### Scope (선택사항)
변경이 영향을 미치는 범위를 명시합니다.

예: `feat(auth):`, `fix(database):`

### Subject (필수)
- 50자 이내의 간결한 설명
- 명령조로 작성 (예: "added" → "add")
- 첫 글자는 소문자
- 마침표(.)로 끝내지 않음

### Body (선택사항)
- 변경 사항에 대한 상세한 설명
- 왜 변경했는지, 어떻게 변경했는지 설명
- 72자마다 줄바꿈

### Footer (선택사항)
- Issue 추적: `Closes #123`
- Breaking Change: `BREAKING CHANGE: ...`

## 예시

```
feat(login): add email validation

Add email format validation to the login form.
This ensures only valid email addresses are accepted.

Closes #45
```

```
fix(database): resolve connection timeout issue

Increased connection pool size from 10 to 20 to handle
higher concurrent requests.

Fixes #67
```

## 규칙
- 한 commit은 하나의 논리적 변경만 포함
- 작고 의미 있는 단위로 commit 작성
- commit 히스토리가 읽기 쉽도록 유지
- **Commit Message는 한글을 사용합니다**
- **헤더는 < > 문자를 사용합니다**

### 한글 Commit Message 예시

```
<fix> 긴급 Fix

로그인 페이지의 이메일 검증 버그를 수정했습니다.
유효하지 않은 이메일도 통과되는 문제를 해결했습니다.

Closes #45
```

```
<feat> 사용자 인증 기능 추가

JWT 토큰 기반의 사용자 인증 시스템을 구현했습니다.
로그인, 로그아웃, 토큰 갱신 기능이 포함됩니다.

Closes #89
```

```
<refactor> 데이터베이스 연결 로직 리팩토링

데이터베이스 연결 풀 크기를 10에서 20으로 증가시켜
높은 동시 요청을 처리할 수 있도록 개선했습니다.

Fixes #67
```
