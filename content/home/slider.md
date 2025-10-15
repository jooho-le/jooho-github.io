---
# 홈 배경 슬라이더
# 사용법
# 1) 사진 넣기: Mac/Windows에서 `static/uploads/slider/` 폴더에 사진 파일을 넣어요.
#    - 예: slide1.jpg, slide2.jpg, slide3.jpg
# 2) 아래 slides에서 '제목/설명/버튼링크'만 바꿔요.
#    - 'background.image'는 사진 경로예요. 파일명만 바꾸면 돼요.
# 3) 슬라이드 더 만들고 싶으면 맨 아래 항목 하나를 복사해서 붙여넣기!
# 4) 삭제하고 싶으면 해당 슬라이드 덩어리를 통째로 지워요.
widget: slider
headless: true
weight: 10

title: ''
subtitle: ''

content:
  slides:
    # [슬라이드 1] — 가장 상단 이미지 (제목/설명만 수정)
    - title: 'Home'
      content: '홈 상단 소개 한 줄을 적어주세요.'
      # 슬라이드 배경 이미지 (파일명만 바꿔요)
      background:
        image: 'uploads/slider/slider1.jpg'  
        brightness: 0.35                    
      cta:
        label: '더 알아보기'
        url: 'about/'

    # [슬라이드 2] — 1화면 아래 이미지 (제목/설명만 수정)
    - title: 'Preview'
      content: '소개/활동 미리보기 한 줄.'
      background:
        image: 'uploads/slider/slider2.jpg'
        brightness: 0.35
      cta:
        label: 'Activity'
        url: 'experience/'

    # [슬라이드 3] — 프로젝트 안내 이미지
    - title: 'Projects'
      content: '아래에서 프로젝트를 확인해 보세요.'
      background:
        image: 'uploads/slider/slider3.jpg'
        brightness: 0.35
      cta:
        label: 'Projects'
        url: '#portfolio'
---
