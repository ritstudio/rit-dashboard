# RIT Dashboard — 배포 지시서

## 목표
이 프로젝트를 GitHub 레포지토리에 올리고 Vercel로 배포한다.

## 실행 순서

### 1. Git 초기화 및 커밋
```bash
git init
git add .
git commit -m "feat: RIT Studio 재무 대시보드 초기 배포"
```

### 2. GitHub 레포 생성 및 푸시
GitHub CLI(gh)가 있으면:
```bash
gh repo create rit-dashboard --public --source=. --push
```

gh가 없으면 아래 순서:
```bash
# 사용자에게 GitHub에서 'rit-dashboard' 레포 생성 후 URL 알려달라고 요청
# 받은 URL로:
git remote add origin https://github.com/[username]/rit-dashboard.git
git branch -M main
git push -u origin main
```

### 3. Vercel 배포
Vercel CLI가 없으면 먼저 설치:
```bash
npm install -g vercel
```

배포:
```bash
vercel --prod --yes
```

프로젝트명: `rit-dashboard`
프레임워크: Other (Static)

### 4. 완료 확인
배포 완료 후 발급된 `.vercel.app` URL을 사용자에게 알려준다.

## 파일 구조
- `index.html` — 메인 대시보드
- `vercel.json` — Vercel 설정
- `CLAUDE.md` — 이 파일
