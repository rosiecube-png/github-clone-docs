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

## 결정 기록은 아직 없습니다

**ADR은 아키텍처 설계 단계의 산출물입니다.** 이 프로젝트는 아직 헌장과
요구사항 단계에 있으므로 `adr/` 디렉터리를 두지 않습니다.

한때 다섯 건을 ADR로 썼다가 걷어냈습니다. 두 가지가 잘못돼 있었습니다.

- 그중 둘(Rust 채택, GitHub 호환)은 **사용자가 준 제약**이지 우리가 대안을
  비교해 고른 결정이 아니었습니다. ADR 형식에 맞추느라 하지도 않은 대안 비교의
  서사를 만든 셈입니다. 제자리는 `CON-07`·`CON-08`입니다.
- 나머지 셋은 진짜 아키텍처 결정이지만, **전제인 가정 17개가 전부 미검증인
  상태에서** 요구사항 단계에 내려졌습니다. 그 대가가 바로 나타났습니다 —
  DB 방침이 경량성 잠정 수치를 무효화했습니다. 미검증 가정을 검증하는 대신
  결정으로 덮어버린 것입니다.

지금 단계에서 결정은 아래에 남습니다.

| 성격 | 어디에 |
| --- | --- |
| 외부에서 주어졌거나 우리가 택한 **지켜야 할 것** | Project의 `CON` 항목 |
| 아직 못 정한 것과 **방침만 정한 것** | [requirements/open-questions.md](requirements/open-questions.md) |
| 참이라고 믿지만 확인 안 된 것 | Project의 `ASM` 항목 |

아키텍처 단계에 진입하면 그때 `adr/`을 다시 엽니다. 방침으로 남겨 둔 것들이
그 단계의 첫 입력입니다.

## 현재 상태

단계 0(기반) 진행 중입니다. 언어와 호환 방침이 정해졌고,
웹 프런트엔드 방식·데이터베이스·CI 격리 방식이 미결입니다.

프로젝트 헌장은 [Project #3](https://github.com/users/rosiecube-png/projects/3)의
README에 있습니다.
