# 🔥 소방시설 개선 관리대장 - 외부 접속 배포 가이드

## 📌 배포 방법 (무료, 5분 이내)

아래 3가지 방법 중 하나를 선택하세요. **모두 무료**이며, 배포 후 외부에서 URL로 접속 가능합니다.

---

## 방법 1: GitHub Pages (추천 ⭐)

### 단계별 진행

1. **GitHub 계정 생성** (이미 있으면 건너뛰기)
   - https://github.com 접속 → Sign up

2. **새 저장소(Repository) 생성**
   - 우측 상단 "+" → "New repository"
   - Repository name: `fire-safety` (원하는 이름)
   - Public 선택
   - "Create repository" 클릭

3. **파일 업로드**
   - "uploading an existing file" 클릭
   - `index.html` 파일을 드래그앤드롭
   - "Commit changes" 클릭

4. **GitHub Pages 활성화**
   - Settings → Pages (왼쪽 메뉴)
   - Source: "Deploy from a branch"
   - Branch: `main` / `/(root)` 선택
   - Save 클릭

5. **접속 확인** (1~2분 후)
   ```
   https://[계정이름].github.io/fire-safety/
   ```

---

## 방법 2: Netlify Drop (가장 쉬움 ⭐)

### 단계별 진행

1. https://app.netlify.com/drop 접속
2. `index.html` 파일이 있는 폴더를 브라우저에 **드래그앤드롭**
3. 자동 배포 완료! URL이 즉시 생성됩니다
   ```
   https://랜덤이름.netlify.app
   ```
4. (선택) Site settings → Change site name에서 URL 변경 가능

> ⚠️ 무료 계정 로그인 없이도 가능하지만, 로그인하면 URL을 영구 유지할 수 있습니다.

---

## 방법 3: Vercel (개발자 추천)

### 단계별 진행

1. https://vercel.com 접속 → 회원가입 (GitHub 계정 연동 가능)
2. "New Project" → "Upload" 선택
3. `index.html` 파일을 업로드
4. "Deploy" 클릭
5. 배포 완료! URL:
   ```
   https://프로젝트이름.vercel.app
   ```

---

## 🔗 개선보고 링크 공유 방법

배포 후 담당자에게 보내는 개선보고 링크 형식:

```
https://[배포된URL]/?report=F-0001
```

예시:
```
https://myname.github.io/fire-safety/?report=F-0001
```

이 링크를 카카오톡, 문자, 이메일로 전달하면 됩니다.

---

## 💾 데이터 관리 주의사항

### 현재 저장 방식
- 데이터는 **각 브라우저의 localStorage**에 저장됩니다
- 같은 기기 + 같은 브라우저에서만 데이터가 유지됩니다

### 데이터 백업
- 관리대장 화면의 **"📥 데이터 내보내기"** 버튼으로 JSON 파일 백업
- **"📤 데이터 가져오기"** 버튼으로 복원 가능

### 여러 기기에서 사용하려면
1. 기기 A에서 "데이터 내보내기"
2. JSON 파일을 기기 B로 전송
3. 기기 B에서 "데이터 가져오기"

---

## 🔧 향후 확장 (서버 연동 시)

현재는 클라이언트(브라우저) 전용이지만, 다음과 같이 확장 가능합니다:

| 확장 방향 | 기술 | 효과 |
|-----------|------|------|
| Google Sheets 연동 | Apps Script API | 실시간 공유 대장 |
| Firebase 연동 | Firestore | 다중 사용자 실시간 동기화 |
| Supabase 연동 | PostgreSQL | 본격 데이터베이스 |

필요 시 요청해 주시면 서버 연동 버전도 만들어 드립니다.
