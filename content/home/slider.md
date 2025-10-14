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
weight: 20

title: ''
subtitle: ''

content:
  slides:
    # [슬라이드 1] — 여기를 수정하세요
    - title: 'Home'
      content: '이주호의  홈페이지에 오신걸 환영합니다.'
      # 슬라이드 배경 이미지 (파일명만 바꿔요)
      background:
        image: '/uploads/slider/slide1.jpg'  
        brightness: 0.35                    
      cta:
        label: '버튼 이름(선택)'              # 예: 더 알아보기
        url: '/about/'                        # 버튼을 누르면 갈 주소

    # [슬라이드 2]
    - title: '여기에 제목(예: Activity)'
      content: '동아리·수상·자격증 등 하이라이트 한 줄.'
      background:
        image: '/uploads/slider/slide2.jpg'
        brightness: 0.35
      cta:
        label: 'Activity'
        url: '/experience/'

    # [슬라이드 3]
    - title: '여기에 제목(예: Projects)'
      content: '최근 진행 프로젝트를 확인해 보세요.'
      background:
        image: '/uploads/slider/slide3.jpg'
        brightness: 0.35
      cta:
        label: 'Projects'
        url: '/#portfolio'
---
