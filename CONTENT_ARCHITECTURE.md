# Content Architecture

공개/비공개 표면의 역할, 연결 관계, 콘텐츠 배치 원칙을 정의하는 청사진.
각 표면의 실제 업데이트는 이 문서를 기준으로 이슈 사이클을 통해 진행한다.

## 정체성 (Identity)

> 이 섹션은 사용자가 직접 작성합니다.

- **한 줄 소개**: (예: 백엔드 개발자, AI 기반 개발 흐름을 실험하고 기록합니다)
- **핵심 키워드**: (예: Backend, AI, DevEx, 이슈 사이클)
- **내러티브**: (예: 코드보다 판단, 도구보다 사고 방식에 집중)

## 표면 정의 (Surface Map)

### 공개 표면

| 표면 | 위치 | 역할 | 대상 |
|------|------|------|------|
| **GitHub Profile README** | [idean3885/idean3885](https://github.com/idean3885/idean3885) | 허브 — 30초 요약, 진입점 | GitHub 방문자 |
| **Blog Repo About** | idean3885.github.io repo settings | 메타데이터 — 검색/탐색 노출 | GitHub 검색 |
| **Blog About 페이지** | [_tabs/about.md](https://idean3885.github.io/about/) | 깊이 — 자기소개, 시리즈 가이드, 프로젝트 | 블로그 방문자 |

### 비공개 표면

| 표면 | 위치 | 역할 | 대상 |
|------|------|------|------|
| **포트폴리오/이력서** | [idean3885/career-docs](https://github.com/idean3885/career-docs) (private) | 커리어 중심 정리 | 채용/네트워킹 |

> **주의**: career-docs는 대외비로 관리한다.
> 공개 표면에서 career-docs의 존재나 내용을 언급하지 않는다.

## 정보 흐름 (Information Flow)

```
GitHub Profile README (허브)
  ├──→ Blog (블로그 링크)
  └──→ Projects (프로젝트 링크)

Blog About 페이지 (깊이)
  ├──→ 시리즈별 포스트 링크
  ├──→ 프로젝트 링크
  └──→ GitHub Profile 링크

Blog Repo About (메타데이터)
  └──→ Blog homepage URL

career-docs (비공개, 독립)
  └── 공개 표면과 직접 연결하지 않음
```

**원칙**: 허브(Profile README)에서 스포크(블로그, 프로젝트)로 연결한다.
깊이 있는 내용은 각 스포크에 두고, 허브는 요약과 링크만 유지한다.

## 콘텐츠 배치 원칙 (Placement Rules)

### 무엇이 어디에 들어가는가

| 콘텐츠 | Profile README | Blog About | Blog Repo About | career-docs |
|--------|:-:|:-:|:-:|:-:|
| 자기소개 (한 줄) | O | O | - | O |
| 자기소개 (상세) | - | O | - | O |
| Tech Stack | O | - | - | O |
| 프로젝트 목록 | O (핵심만) | O (전체) | - | O |
| 포스트 목록 | O (최신 자동) | O (시리즈별) | - | - |
| 카테고리 구조 | - | O | - | - |
| 블로그 URL | O | - | O | - |
| 커리어 이력 | - | - | - | O |
| topics | - | - | O | - |

### 배치 기준

1. **중복 최소화**: 같은 정보를 여러 곳에 두지 않는다.
   한 곳에 원본을 두고 나머지는 링크로 연결한다.
2. **깊이 분리**: 허브는 요약, 스포크는 상세.
   Profile README에 포스트 전체 목록을 넣지 않는다.
3. **공개/비공개 경계**: career-docs 내용은 공개 표면에 노출하지 않는다.
4. **자동화 우선**: 수동 동기화가 필요한 구조는 피한다.
   (예: Profile README의 블로그 포스트는 RSS 자동 갱신)

## 현황 (Last Updated: 2026-02-23)

| 표면 | 상태 | 미완료 항목 |
|------|------|-------------|
| GitHub Profile README | 초기 상태 | 프로젝트 추가, 포스트 자동화 점검, 내러티브 통일 |
| Blog Repo About | 완료 | - |
| Blog About 페이지 | 구조 완료 | 자기소개 작성 |
| career-docs | 초기 상태 | 전체 구성 |

## 워크플로우

```
1. 이 문서(청사진) 수정
2. 변경이 필요한 표면 식별
3. 각 표면의 레포에서 이슈 사이클로 업데이트
4. 완료 후 이 문서의 "현황" 섹션 반영
```
