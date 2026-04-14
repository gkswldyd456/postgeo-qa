# PostGeo QA Dashboard

PostGeo 웹버전 기능 이식 현황 및 QA 상태를 추적하는 대시보드입니다.

## 접속 방법

```
https://gkswldyd456.github.io/postgeo-qa/
```

토큰 없이 누구나 열람 가능합니다. 상태 저장은 토큰 보유자만 가능합니다.

---

## 현황 (2026-04-14 기준)

| 항목 | 수치 |
|------|------|
| 전체 기능 항목 | 163개 (12개 카테고리) |
| 웹 이식 완료 | 101개 (62%) |
| 부분 이식 | 20개 (12%) |
| 미이식 | 42개 (26%) |
| QA 테스트 진행률 | 0% (웹이식 확인 단계) |

---

## 카테고리 구성

| 카테고리 | 항목 수 | 이식 완료 |
|----------|:-------:|:--------:|
| 점 (Points) | 25 | 23 |
| 선/선분 (Lines) | 21 | 17 |
| 평면도형 (Plane Figures) | 30 | 16 |
| 입체도형 (3D Figures) | 6 | 0 |
| 점 기반 함수 (Point Functions) | 30 | 24 |
| 입력 기반 함수 (Input Functions) | 7 | 7 |
| 캔버스/편집 기능 (Canvas & Edit) | 15 | 6 |
| 캔버스 설정 (Canvas Settings) | 7 | 6 |
| 파일/저장 (File & Save) | 5 | 0 |
| 텍스트/이미지 (Text & Image) | 5 | 0 |
| 확률 탁자 순열 (Probability Tables) | 10 | 0 |
| 설정 (Settings) | 2 | 2 |

---

## 대시보드 기능

| 기능 | 설명 |
|------|------|
| 상태 뱃지 클릭 | 웹이식 / QA 상태 순환 변경 |
| 💾 저장 | GitHub에 변경사항 저장 (토큰 필요) |
| 필터 | 카테고리 · 웹이식 · 구현상태 · QA 상태별 필터링 |
| 컬럼 리사이즈 | 헤더 경계 드래그로 너비 조정 (localStorage 저장) |
| 컬럼 가이드 ⓘ | 각 컬럼 헤더 클릭 시 체크 기준 팝오버 |
| 편집 모드 ✏ | 항목 이름 수정 / 삭제 / 순서 변경 (드래그앤드롭) |
| 인라인 삽입 | 편집 모드에서 행 사이 hover → ＋ 위치 추가 |
| 이슈/메모 | 셀 클릭으로 이슈 번호 + 메모 편집 |
| 전체 코멘트 탭 | 특정 기능과 무관한 전반적 의견 기록 |
| 코멘트 타입 관리 | 설정에서 타입 추가/삭제 |

---

## 상태값 순환

| 컬럼 | 순환 |
|------|------|
| 웹이식 | `? 미확인` → `✓ 완료` → `△ 부분` → `✗ 미이식` |
| 구현상태 | `미시작` → `계획` → `진행중` → `완료` |
| QA | `미테스트` → `통과` → `실패` → `건너뜀` |

---

## GitHub Pages 설정 (최초 1회)

1. 저장소 **Settings** → **Pages**
2. Source: **Deploy from a branch** → `main` / `/ (root)` → **Save**
3. 1~2분 후 URL 활성화

## Personal Access Token 발급

저장 기능 사용 시 필요합니다.

1. GitHub 프로필 → **Settings** → **Developer settings**
2. **Personal access tokens** → **Tokens (classic)**
3. **Generate new token (classic)** → Scopes: `public_repo` 체크 → 생성
4. 대시보드 **⚙ 설정**에 토큰 입력

---

## 관련 저장소

- **QA 대시보드**: `gkswldyd456/postgeo-qa` (이 저장소)
- **개발자 저장소**: `Post-Math/PostGeoWeb` (이슈 등록 대상)

---

*Built with GitHub Pages + Vanilla JS*
