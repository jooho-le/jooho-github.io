---
# 홈 배경 슬라이더(이미지 우선 구성)
# - 아래 `slides` 항목의 이미지 파일을 `static/uploads/slider/` 폴더에 추가하세요.
# - 예) slide1.jpg, slide2.jpg, slide3.jpg 파일을 넣으면 자동으로 표시됩니다.
widget: slider
headless: true
weight: 20

title: ''
subtitle: ''

slides:
  - title: 'Medical AI'
    content: '의료 인공지능 관련 연구/프로젝트 개요 문구를 입력하세요.'
    # 슬라이드 배경 이미지 경로(정적 폴더 기준)
    background:
      image: '/uploads/slider/slide1.jpg'
      # 어둡게 오버레이 적용 비율(0~1)
      brightness: 0.35
    cta:
      label: '더 알아보기'
      url: '/about/'

  - title: 'Activity'
    content: '동아리·수상·자격증 등 활동 하이라이트 문구를 입력하세요.'
    background:
      image: '/uploads/slider/slide2.jpg'
      brightness: 0.35
    cta:
      label: 'Activity'
      url: '/experience/'

  - title: 'Projects'
    content: '최근 진행 프로젝트를 확인해 보세요.'
    background:
      image: '/uploads/slider/slide3.jpg'
      brightness: 0.35
    cta:
      label: 'Projects'
      url: '/#portfolio'
---

