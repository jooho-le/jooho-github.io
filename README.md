## 이주호 포트폴리오 (Hugo + HugoBlox)

- 배포 주소: https://jooho-le.github.io/jooho-github.io/
- 목적: Medical AI, AI, Data Engineering, Development, Embedded 활동/프로젝트/이력 소개

### 구조
- 홈(슬라이더, 하이라이트 카드, 인터레스트, 경험 요약)
- About(프로필, 관심분야, 학위, 기술/스택, 타임라인, 연락처·지도)
- Projects, Awards, Skills, Experience, Qualifications

### 실행(로컬)
1) Hugo Extended 설치(워크플로 기준 0.124.x 권장)
2) 개발 서버 실행
   - `hugo server -D`
3) 브라우저에서 `http://localhost:1313/` 접속

### 배포(GitHub Pages)
- 기본 브랜치 `main`에 푸시 → `.github/workflows/publish.yaml`가 빌드/배포
- 프로젝트 사이트 URL에 맞춰 `config/_default/hugo.yaml`의 `baseURL` 설정됨

### 콘텐츠 편집 가이드
- 홈 슬라이더: `content/home/slider/index.md`
  - 배경 이미지: 정적 경로 `/uploads/slider/slider*.jpg` 사용
  - 슬라이드 추가 시 `slides:` 항목 복사/수정
- 하이라이트 카드: `content/home/overlay_cards.md`
- 경험 카드: `content/home/experience_cards.md`
- 인터레스트: `content/home/interests.md`
- About 연락처/지도: `content/about/contact_map.md`

### 에셋 경로
- 정적 이미지(슬라이더/카드용): `static/uploads/slider/`
- 사이트 로고: `assets/media/logo.png` (또는 `logo.svg`)
- 이력서 PDF: `static/uploads/resume.pdf`

### SEO/검색 등록
- Search Console HTML 파일: `static/google*.html` 유지
- 사이트맵: `/sitemap.xml` (프로젝트 URL 기준)

### 라이선스/테마
- 본 저장소는 HugoBlox(Wowchemy) 기반 템플릿을 커스터마이즈했습니다.

문의: 이슈 또는 메일 `wngh9696@naver.com`
