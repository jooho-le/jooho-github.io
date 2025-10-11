---
# 수상(Award) 섹션 — 카드형(Portfolio 위젯)
widget: portfolio
headless: true
weight: 10

title: 수상 내역
subtitle: 카드를 클릭하면 상세 내용과 사진을 볼 수 있습니다.

content:
  # award 타입의 페이지만 카드로 수집해 보여줍니다.
  page_type: award
  filter_default: 0

design:
  columns: '1'   # 1열(세로 카드)
  view: masonry  # 카드 배치 스타일
  flip_alt_rows: false
  background: {}
  spacing: {padding: [0, 0, 0, 0]}
---

