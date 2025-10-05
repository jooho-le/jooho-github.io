---
# 작성자 프로필 (히어로/포스트 하단 등에서 사용)

# 표시 이름 (ex. 홍길동)
title: 내 이름을 입력하세요

# 사이트의 기본 사용자 여부 (단일 사용자 사이트면 true 유지)
superuser: true

# 직무/포지션 (ex. 머신러닝 엔지니어)
role: ''

# 상태 이모지 (선택)
status:
  icon: ☕️

# 한 줄 소개/간단 소개 (프로필 카드/포스트 하단에 표시)
bio: 한 줄 소개를 입력하세요.

# 소셜/링크 아이콘
# - 사용 가능한 아이콘: docs 참고
# - 이메일 링크는 `mailto:example@domain.com` 형태 사용
social:
  - icon: envelope
    icon_pack: fas
    link: 'about/#contact'  # 연락처 위젯으로 이동. 직접 메일은 mailto 사용
  #- icon: github
  #  icon_pack: fab
  #  link: https://github.com/<사용자명>
  #- icon: linkedin
  #  icon_pack: fab
  #  link: https://www.linkedin.com/in/<사용자명>/
  #- icon: instagram
  #  icon_pack: fab
  #  link: https://instagram.com/<사용자명>

# 이력서 PDF 링크(선택)
# - `static/uploads/resume.pdf` 위치에 파일 두고 아래 주석 해제
# - icon: cv
#   icon_pack: ai
#   link: uploads/resume.pdf
---
여기에 자기소개 본문을 한국어로 자유롭게 적어주세요.
프로젝트 관심사, 경력, 목표 등을 간단히 서술하면 좋습니다.

{{< icon name="download" pack="fas" >}} {{< staticref "uploads/resume.pdf" "newtab" >}}이력서 다운로드{{< /staticref >}}
