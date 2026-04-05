# Content Architecture

공개 표면의 역할, 연결 관계, 콘텐츠 배치 원칙을 정의하는 청사진.

각 표면의 실제 업데이트는 이 문서를 기준으로 이슈 사이클을 통해 진행한다.

## 정체성 (Identity)

- **한 줄 소개**: Spring Boot + Kubernetes 기반 MSA 환경에서 서비스를 설계하고 운영하는 백엔드 개발자
- **핵심 키워드**: 백엔드, MSA, AI 도구 설계, 판단과 설계, 비판적 사고
- **내러티브**: AI 시대에 개발자의 가치는 판단과 설계에 있다고 생각합니다. 이를 검증하기 위해 개발 방법론과 도구를 직접 만들고, 그 과정을 블로그에 기록하고 있습니다.

## 표면 정의 (Surface Map)

| 표면 | 위치 | 역할 | 대상 |
|------|------|------|------|
| **GitHub Profile README** | [idean3885/idean3885](https://github.com/idean3885/idean3885) | 허브 — 30초 요약, 진입점 | GitHub 방문자 |
| **Blog Repo About** | blog.idean.me repo settings | 메타데이터 — 검색/탐색 노출 | GitHub 검색 |
| **Blog About (홈 소개 섹션)** | [홈 페이지 소개 영역](https://blog.idean.me) | 깊이 — 자기소개, 포커스 영역 안내 | 블로그 방문자 |

## 정보 흐름 (Information Flow)

```
GitHub Profile README (허브)
  ├──→ Blog (블로그 링크)
  └──→ Projects (프로젝트 링크)

Blog 홈 소개 섹션 (깊이)
  ├──→ 포커스 영역별 포스트 링크
  └──→ 주요 포스팅 링크

Blog Repo About (메타데이터)
  └──→ Blog homepage URL
```

**원칙**: 허브(Profile README)에서 스포크(블로그, 프로젝트)로 연결한다.

깊이 있는 내용은 각 스포크에 두고,
허브는 요약과 링크만 유지한다.

## 콘텐츠 배치 원칙 (Placement Rules)

### 무엇이 어디에 들어가는가

| 콘텐츠 | Profile README | Blog 홈 소개 | Blog Repo About |
|--------|:-:|:-:|:-:|
| 자기소개 (한 줄) | O | O | - |
| 자기소개 (상세) | - | O | - |
| Tech Stack | O | - | - |
| 프로젝트 목록 | O (핵심만) | - | - |
| 포스트 목록 | O (대표 큐레이션) | O (주요 포스팅) | - |
| 포커스 영역 | - | O | - |
| 블로그 URL | O | - | O |
| topics | - | - | O |

### 배치 기준

1. **중복 최소화**: 같은 정보를 여러 곳에 두지 않는다.
   한 곳에 원본을 두고 나머지는 링크로 연결한다.
2. **깊이 분리**: 허브는 요약, 스포크는 상세.
   Profile README에 포스트 전체 목록을 넣지 않는다.
3. **큐레이션 우선**: Profile README의 포스트는 대표성 있는 글만 수동 관리한다.
   무차별 자동 수집은 허브 역할에 부적합하다.

## 현황 (Last Updated: 2026-03-29)

| 표면 | 상태 | 미완료 항목 |
|------|------|-------------|
| GitHub Profile README | 완료 | - |
| Blog Repo About | 완료 | - |
| Blog About (홈 소개 섹션) | 완료 | - |

## 워크플로우

```
1. 이 문서(청사진) 수정
2. 변경이 필요한 표면 식별
3. 각 표면의 레포에서 이슈 사이클로 업데이트
4. 완료 후 이 문서의 "현황" 섹션 반영
```
