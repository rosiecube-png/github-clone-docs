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

## 현재 상태

저장소 초기화 단계입니다. 아직 작성된 명세는 없습니다.
