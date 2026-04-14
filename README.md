# PostGeo QA Dashboard

PostGeo 웹버전 기능 이식 현황 및 QA 상태를 추적하는 대시보드입니다.

## 접속 방법

GitHub Pages 활성화 후 아래 URL로 접속합니다.

```
https://{내_GitHub_아이디}.github.io/postgeo-qa/
```

---

## 처음 설정하기 (GitHub 초심자 가이드)

### 1단계 — 저장소 만들기

1. [github.com](https://github.com) 로그인
2. 우측 상단 **+** → **New repository** 클릭
3. Repository name: `postgeo-qa`
4. **Public** 선택 ✓ (개발자분도 링크로 바로 볼 수 있어야 함)
5. **Create repository** 클릭

### 2단계 — 파일 올리기

저장소 메인 페이지에서:

1. **uploading an existing file** 클릭 (또는 Add file → Upload files)
2. 아래 두 파일을 드래그해서 올리기:
   - `index.html`
   - `qa-data.json`
3. 하단 **Commit changes** 클릭

### 3단계 — GitHub Pages 켜기

1. 저장소 상단 **Settings** 탭 클릭
2. 왼쪽 메뉴 **Pages** 클릭
3. Source: **Deploy from a branch** 선택
4. Branch: **main** / **/ (root)** 선택 → **Save**
5. 1~2분 후 상단에 URL 표시됨

### 4단계 — Personal Access Token 발급

대시보드에서 상태를 저장하려면 토큰이 필요합니다.

1. GitHub 우측 상단 프로필 → **Settings**
2. 왼쪽 맨 아래 **Developer settings**
3. **Personal access tokens** → **Tokens (classic)**
4. **Generate new token (classic)** 클릭
5. Note: `PostGeoQA`
6. Expiration: `90 days` (또는 원하는 기간)
7. Scopes: **public_repo** 체크 ✓
8. **Generate token** → 생성된 토큰 복사 (화면 닫으면 다시 못 봄!)

### 5단계 — 대시보드 첫 설정

1. 대시보드 URL 접속
2. 우측 상단 **⚙ 설정** 버튼 클릭
3. 입력:
   - **내 GitHub 사용자명**: 내 아이디
   - **Personal Access Token**: 4단계에서 복사한 토큰
   - **개발자 GitHub 저장소**: 개발자분 저장소 주소 (예: `devuser/postgeo-web`)
4. **저장 후 새로고침** 클릭

---

## 사용 방법

### 상태 변경
각 기능 행의 **뱃지를 클릭**하면 상태가 순환됩니다.

| 열 | 클릭 순서 |
|----|-----------|
| 웹이식 | `? 미확인` → `✓ 완료` → `△ 부분` → `✗ 미이식` → (반복) |
| 구현상태 | `미시작` → `계획` → `진행중` → `완료` → (반복) |
| QA | `미테스트` → `통과` → `실패` → `건너뜀` → (반복) |

### 이슈 연결
- **이슈/메모** 열 클릭 → 이슈 번호 입력 (예: `3, 7`)
- 개발자 저장소 설정 시 → 자동으로 클릭 가능한 링크로 표시

### 저장
- 상태 변경 후 우측 상단 **💾 저장** 클릭
- 헤더에 `● 미저장` 표시 = 저장 안 된 변경사항 있음
- `✓ 저장됨` 표시 = GitHub에 성공적으로 저장됨

### 필터
- 카테고리, 웹이식 여부, 구현상태, QA 상태별로 필터링 가능

---

## 카테고리 구성

| 카테고리 | 항목 수 |
|----------|---------|
| 점 (Points) | 31 |
| 선/선분 (Lines) | 22 |
| 평면도형 (Plane Figures) | 30 |
| 입체도형 (3D Figures) | 6 |
| 점 기반 함수 (Point Functions) | 31 |
| 입력 기반 함수 (Input Functions) | 11 |
| 캔버스/편집 기능 | 15 |
| 캔버스 설정 | 7 |
| 파일/저장 | 5 |
| 텍스트/이미지 | 5 |
| 확률 탁자 순열 | 10 |
| 설정 | 2 |

---

## 개발자분께

이 대시보드는 QA 테스터가 운영하는 별도 저장소입니다.  
기능 이식 완료 시 해당 항목의 상태를 업데이트해주시거나,  
이슈는 기존 저장소 Issues 탭에 등록해주세요.

---

*Built with GitHub Pages + Vanilla JS*
