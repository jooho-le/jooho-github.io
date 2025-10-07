---
## About 위젯 (프로필 + 소개)
# - seoharu 스타일처럼 프로필을 좌측(또는 상단)에, 소개를 우측(또는 하단)에 표시합니다.
# - 프로필(이름/사진/직무/소속/소셜)은 `content/authors/admin/_index.md`에서 관리합니다.
# - 이 파일은 섹션의 제목/배치/배경 등을 제어합니다.
widget: about

# 위젯 활성화 여부
active: true

# 위젯 페이지의 섹션 파일임을 의미
headless: true

# 섹션 순서 (값이 작을수록 위쪽)
weight: 10

# 섹션 제목(필요 없으면 공백으로 두세요)
title: 소개

# 표시할 작성자(프로필) ID — `content/authors/` 내부 폴더명
author: admin

# 디자인 옵션(배경/컬럼 등)
design:
  columns: '1'
  background:
    color: ''   # 예: '#111418' (어두운 배경). 비우면 기본값 사용
---
