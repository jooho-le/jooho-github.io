## 이주호 포트폴리오 

- 배포 주소: https://jooho-le.github.io/jooho-github.io/
- 목적: Medical AI, AI, Data Engineering, Development, Embedded 활동/프로젝트/이력 소개

### 구조
- 홈(슬라이더, 하이라이트 카드, 인터레스트, 경험 요약)
- About(프로필, 관심분야, 학위, 기술/스택, 타임라인, 연락처·지도)
- Projects, Awards, Skills, Experience, Qualifications

### 콘텐츠 편집 가이드
- 홈 슬라이더: `content/home/slider/index.md`
  - 배경 이미지: 정적 경로 `/uploads/slider/slider*.jpg` 사용
  - 슬라이드 추가 시 `slides:` 항목 복사/수정
- 하이라이트 카드: `content/home/overlay_cards.md`
- 경험 카드: `content/home/experience_cards.md`
- 인터레스트: `content/home/interests.md`
- About 연락처/지도: `content/about/contact_map.md`


### SEO/검색 등록
- Search Console HTML 파일: `static/google*.html` 유지
- 사이트맵: `/sitemap.xml` (프로젝트 URL 기준)

### 라이선스/테마
- 본 저장소는 HugoBlox(Wowchemy) 기반 템플릿을 커스터마이즈했습니다.

문의: 이슈 또는 메일 `wngh9696@naver.com`

## 프로젝트 구조

```
.
├─ .github/
│  └─ workflows/
│     └─ publish.yaml                # GitHub Pages 배포 워크플로
├─ assets/
│  ├─ media/
│  │  ├─ icon.png                    # 파비콘(브라우저 탭 아이콘)
│  │  ├─ logo.png                    # 사이트/OG 기본 로고 이미지
│  │  └─ slider*.jpg(.jpeg)          # 예비 이미지(리소스)
│  └─ scss/
│     └─ template.scss               # 커스텀 스타일(레이아웃/버튼/슬라이더 등)
├─ config/_default/
│  ├─ hugo.yaml                      # 사이트 기본 설정(baseURL, title 등)
│  ├─ params.yaml                    # 마케팅/SEO/헤더/푸터 등 전역 파라미터
│  ├─ languages.yaml                 # ko/en 언어 설정
│  ├─ menus.yaml                     # 헤더 메뉴
│  └─ module.yaml                    # Hugo 모듈
├─ content/
│  ├─ home/
│  │  ├─ index.md                    # 홈 위젯 페이지
│  │  ├─ slider/index.md             # 홈 슬라이더 구성
│  │  ├─ overlay_cards.md            # 홈 하이라이트 카드(Blank)
│  │  ├─ experience_cards.md         # 홈 경험 카드(Blank)
│  │  ├─ interests.md                # 홈 관심사 카드(Blank)
│  │  ├─ intro.md                    # 홈 히어로(about.avatar)
│  │  ├─ portfolio.md                # 프로젝트 카드(Portfolio 위젯)
│  │  ├─ slider_autoplay.md          # 슬라이더 자동/화살표 제어 스크립트
│  │  └─ translate.md                # EN 전환 시 자동 번역 스니펫
│  ├─ about/
│  │  ├─ about.md                    # about 위젯(작성자 카드)
│  │  ├─ hero.md                     # About 상단 커스텀 히어로(Blank)
│  │  ├─ interests.md                # 관심사(Blank)
│  │  ├─ tech.md                     # 언어/기술(Blank+bars)
│  │  ├─ skills.md                   # 스킬(Blank+bars)
│  │  ├─ education_timeline.md       # 교육 타임라인(Blank)
│  │  ├─ contact_map.md              # 연락처/지도(Blank)
│  │  ├─ summary.md                  # 소개 텍스트(Blank)
│  │  └─ translate.md                # EN 전환 번역 스니펫
│  ├─ project/
│  │  ├─ campuslink/index.md         # 프로젝트 페이지 번들(+featured.*)
│  │  ├─ medimate/index.md
│  │  └─ readandlead/index.md
│  ├─ award/
│  │  ├─ awards.md                   # 수상 카드(Portfolio 위젯)
│  │  ├─ index.md                    # Award 섹션 페이지
│  │  └─ translate.md
│  ├─ experience/
│  │  ├─ index.md
│  │  ├─ experience.md               # 경험(Experience 위젯 데이터)
│  │  └─ translate.md
│  ├─ skills/
│  │  ├─ index.md
│  │  ├─ skills.md                   # 자유서술 스킬(Blank)
│  │  └─ translate.md
│  └─ authors/admin/
│     ├─ _index.md                   # 작성자 프로필
│     └─ avatar.png                  # 프로필 이미지
├─ static/
│  ├─ uploads/
│  │  ├─ slider/slider{1,2,3}.jpg    # 슬라이더 배경 이미지(정적 경로)
│  │  └─ resume.pdf                  # 이력서(다운로드)
│  ├─ google*.html                   # Search Console 인증 파일
│  └─ robots.txt                     # robots + Sitemap 경로
└─ README.md
```