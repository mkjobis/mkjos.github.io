# GitHub Pages 배포 가이드

## 방법 1: 웹사이트에서 직접 업로드 (가장 간단)

### 1단계: GitHub 저장소 생성
1. https://github.com 접속
2. 우측 상단 "+" 버튼 클릭 → "New repository"
3. Repository name 입력 (예: `my-portfolio`)
4. **Public** 선택 (GitHub Pages는 Public 저장소에서만 무료)
5. "Create repository" 클릭

### 2단계: 파일 업로드
1. 생성된 저장소 페이지에서 "uploading an existing file" 클릭
2. 또는 "Add file" → "Upload files" 클릭
3. 다음 파일들을 드래그 앤 드롭:
   - `index.html`
   - `styles.css`
   - `script.js`
   - `P.png`
   - `README.md` (선택사항)
4. 하단에 커밋 메시지 입력 (예: "Initial commit")
5. "Commit changes" 클릭

### 3단계: GitHub Pages 활성화
1. 저장소 페이지에서 **Settings** 탭 클릭
2. 왼쪽 메뉴에서 **Pages** 클릭
3. "Source" 섹션에서:
   - Branch: `main` (또는 `master`) 선택
   - Folder: `/ (root)` 선택
4. **Save** 클릭

### 4단계: URL 확인
- 몇 분 후 Settings > Pages 페이지에 배포된 URL이 표시됩니다
- 형식: `https://[사용자명].github.io/[저장소명]/`
- 예: `https://username.github.io/my-portfolio/`

---

## 방법 2: Git 명령어 사용 (터미널)

### 사전 준비
Git이 설치되어 있어야 합니다. 설치 확인:
```bash
git --version
```

### 1단계: 저장소 초기화
```bash
cd /Users/minkyun-jobis/Downloads/08_프로젝트/dev/HTMLCSSJAVASCRIPT
git init
```

### 2단계: 파일 추가 및 커밋
```bash
git add .
git commit -m "Initial commit: 자기소개 페이지"
```

### 3단계: GitHub 저장소와 연결
```bash
# GitHub에서 저장소를 먼저 생성한 후
git remote add origin https://github.com/[사용자명]/[저장소명].git
git branch -M main
git push -u origin main
```

### 4단계: GitHub Pages 활성화
- 방법 1의 3단계와 동일하게 Settings > Pages에서 설정

---

## 중요 사항

1. **저장소는 Public이어야 합니다** (무료 GitHub Pages는 Public 저장소만 지원)
2. **파일명 확인**: `index.html`이 루트 디렉토리에 있어야 합니다
3. **배포 시간**: 처음 배포 시 5-10분 정도 소요될 수 있습니다
4. **업데이트**: 파일을 수정하고 커밋하면 자동으로 재배포됩니다

---

## 문제 해결

### 페이지가 표시되지 않는 경우
- Settings > Pages에서 배포 상태 확인
- URL이 올바른지 확인 (대소문자 구분)
- 브라우저 캐시 삭제 후 다시 시도

### 이미지가 표시되지 않는 경우
- 이미지 파일명이 정확한지 확인 (대소문자 구분)
- 파일 경로가 올바른지 확인

