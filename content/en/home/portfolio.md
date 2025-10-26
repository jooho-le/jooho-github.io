---
# A section created with the Portfolio widget.
# This section displays content from `content/project/`.
# Documentation: https://docs.hugoblox.com/widget/portfolio/
widget: portfolio

# This file defines a page section.
headless: true

# Display order on the homepage (lower number = higher position).
weight: 50

title: 'Projects'
subtitle: 'Featured Project Cards'

content:
  # The type of pages to display (e.g., project).
  page_type: project

  # Default active filter index (e.g., 0 = first filter_button below).
  filter_default: 0

  # Filter toolbar
  # Each filter_button corresponds to a tag.
  # Use '*' to show all projects.
  filter_button:
    - name: All
      tag: '*'
    - name: Web Service
      tag: 'Web service'
    - name: App Service
      tag: 'App service'
    - name: Data Analysis
      tag: 'Data analysis'
    - name: AI
      tag: 'AI'

design:
  columns: '1'
  view: masonry
  flip_alt_rows: true
  background: {}
  spacing: {padding: [0, 0, 0, 0]}
---
