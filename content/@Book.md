---
up:
  - "[[@Homepage]]"
tags:
  - dashboard
dash_type:
  - Source
sort:
  - "40"
created: 2025-09-21
updated: 2025-10-03
dg-publish: true
draft: true
---


```base
filters:
  and:
    - file.hasTag("textbook/index")
    - '!file.inFolder("99 Extension")'
formulas:
  Progress: |
    "■".repeat(((note["current_page"] / note["total_page"]) * 5).round(0)) +
    "□".repeat(5 - ((note["current_page"] / note["total_page"]) * 5).round(0)) +
    " " +
    ((note["current_page"] / note["total_page"]) * 100).round(0).toString() + "%"
views:
  - type: cards
    name: Textbook
    order:
      - file.name
      - formula.Progress
    image: note.img_book
    imageAspectRatio: 1
    cardSize: 150
    imageFit: contain

```


```base
filters:
  and:
    - file.hasTag("book/note")
    - '!file.inFolder("99 Extension")'
formulas:
  Progress: |
    "■".repeat(((note["current_page"] / note["total_page"]) * 5).round(0)) +
    "□".repeat(5 - ((note["current_page"] / note["total_page"]) * 5).round(0)) +
    " " +
    ((note["current_page"] / note["total_page"]) * 100).round(0).toString() + "%"
views:
  - type: cards
    name: Book
    order:
      - file.name
      - formula.Progress
    image: note.img_book
    imageAspectRatio: 1
    cardSize: 150
    imageFit: contain

```

