# github-clone-docs

프로젝트의 명세와 설계 문서를 모으는 저장소입니다.

[github-clone](https://github.com/rosiecube-png/github-clone) 프로젝트의 구성 요소입니다.

## 역할

여러 저장소에 걸친 결정 사항을 한곳에 기록합니다. 코드가 아니라 합의를 담습니다.

## 담을 내용

- **아키텍처** — 구성 요소 간 경계와 호출 관계, 데이터 소유권
- **API 명세** — REST 엔드포인트(OpenAPI), GraphQL 스키마
- **데이터 모델** — 엔티티와 관계, 권한 판정 규칙
- **ADR** — 주요 기술 결정과 그 근거 (Architecture Decision Records)
- **용어집** — 저장소·조직·팀·협업자 등 용어의 정확한 정의

## 저장소 지도

| 저장소 | 역할 |
| --- | --- |
| `github-clone` | 프로젝트 개요, 로드맵 |
| `github-clone-api` | REST·GraphQL 백엔드, 플랫폼 상태 관리 |
| `github-clone-git-server` | Smart HTTP·SSH git 프로토콜 |
| `github-clone-web` | 웹 프런트엔드 |
| `github-clone-cli` | `ghc` 커맨드라인 클라이언트 |
| `github-clone-actions-runner` | 워크플로 실행기 |
| `github-clone-webhooks` | 이벤트 디스패치·알림 |
| `github-clone-docs` | 명세·설계 문서 (이 저장소) |

## 요구사항

**요구사항과 헌장의 원본은 Projects입니다.** 이 저장소에 복제해 두지 않습니다.

- [Project #3 — github-clone](https://github.com/users/rosiecube-png/projects/3)
  — 요구사항 185개(FR 135 · NFR 50), 헌장은 Project README

체계와 필드 정의는 [requirements/README.md](requirements/README.md)를 보세요.

| 문서 | 내용 |
| --- | --- |
| [requirements/open-questions.md](requirements/open-questions.md) | 미결 질문 — 인터뷰 백로그 |

## ADR

주요 기술 결정과 그 근거입니다.

| 번호 | 제목 | 상태 |
| --- | --- | --- |
| [0001](adr/0001-implementation-language-rust.md) | 구현 언어로 Rust를 채택한다 | 채택됨 |
| [0002](adr/0002-github-compatibility.md) | GitHub 호환성을 1급 요구사항으로 채택한다 | 채택됨 |
| [0003](adr/0003-ci-isolation-container-runtime.md) | CI 작업 격리에 컨테이너 런타임을 필수 의존성으로 둔다 | 채택됨 |
| [0004](adr/0004-external-database-by-default.md) | 데이터베이스는 외부 DB를 기본으로 한다 | 채택됨 |
| [0005](adr/0005-actions-admin-import-only.md) | 재사용 액션은 관리자 반입 전용으로 한다 | 채택됨 |

## 현재 상태

단계 0(기반) 진행 중입니다. 언어와 호환 방침이 정해졌고,
웹 프런트엔드 방식·데이터베이스·CI 격리 방식이 미결입니다.

프로젝트 헌장은 [Project #3](https://github.com/users/rosiecube-png/projects/3)의
README에 있습니다.
