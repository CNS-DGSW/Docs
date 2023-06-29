---
sidebar_position: 3
---

# 원서접수 페이지 다이어그램

```mermaid
stateDiagram-v2
    pageProvider: page provider
    note left of pageProvider
        원서접수 페이지와 관련된 상태 및 함수
    end note
    pageProvider --> nav: {currentPage, movePage}
    pageProvider --> currentPageRender: {currentPage}
    pageProvider --> Aside: {currentPage, moveNextPage, movePreviousPage}
    pageProvider --> Title: {currentPage}

    page: write page
    note right of page
        원서접수 페이지
    end note
    nav --> page
    currentPageRender --> page
    Aside --> page
    Title --> page
```
