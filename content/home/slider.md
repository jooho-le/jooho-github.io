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
active: true
headless: true
weight: 10

title: ''
subtitle: ''

content:
  slides:
    # [슬라이드 1] — Home
    - title: 'Home'
      content: |-
        홈으로 이동합니다.
        
        <a class="btn btn-primary" href="./">Home →</a>
      # 슬라이드 배경 이미지 (파일명만 바꿔요)
      background:
        image: 'upload_slider/slider1.jpg'  
        brightness: 0.35                    
      cta:
        label: 'Home'
        url: './'

    # [슬라이드 2] — About
    - title: 'About'
      content: |-
        자기소개와 프로필을 확인해 보세요.
        
        <a class="btn btn-primary" href="about/">About →</a>
      background:
        image: 'upload_slider/slider2.jpg'
        brightness: 0.35
      cta:
        label: 'About'
        url: 'about/'

    # [슬라이드 3] — Projects
    - title: 'Projects'
      content: |-
        홈의 프로젝트 섹션으로 이동합니다.
        
        <a class="btn btn-primary" href="#portfolio">Projects →</a>
      background:
        image: 'upload_slider/slider3.jpg'
        brightness: 0.35
      cta:
        label: 'Projects'
        url: '#portfolio'

    # [슬라이드 4] — Qualifications
    - title: 'Qualifications'
      content: |-
        보유 자격증 목록을 볼 수 있습니다.
        
        <a class="btn btn-primary" href="qualifications/">Qualifications →</a>
      background:
        image: 'upload_slider/slider2.jpg'
        brightness: 0.35
      cta:
        label: 'Qualifications'
        url: 'qualifications/'

    # [슬라이드 5] — Award
    - title: 'Award'
      content: |-
        수상 내역을 확인해 보세요.
        
        <a class="btn btn-primary" href="award/">Award →</a>
      background:
        image: 'upload_slider/slider3.jpg'
        brightness: 0.35
      cta:
        label: 'Award'
        url: 'award/'

    # [슬라이드 6] — Skills
    - title: 'Skills'
      content: |-
        기술 스택과 도구들을 정리했습니다.
        
        <a class="btn btn-primary" href="skills/">Skills →</a>
      background:
        image: 'upload_slider/slider1.jpg'
        brightness: 0.35
      cta:
        label: 'Skills'
        url: 'skills/'

    # [슬라이드 7] — Experience
    - title: 'Experience'
      content: |-
        활동/경험 전체 목록으로 이동합니다.
        
        <a class="btn btn-primary" href="experience/">Experience →</a>
      background:
        image: 'upload_slider/slider2.jpg'
        brightness: 0.35
      cta:
        label: 'Experience'
        url: 'experience/'
---
