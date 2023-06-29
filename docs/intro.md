---
sidebar_position: 1
---

# CNS Frontend Team

CNS 프론트엔드 팀에 문화와 규칙에 대한 글입니다.

## 프론트엔드 팀 문화

(작성중)

## 프론트엔드 팀 규칙

서비스를 개발하며 지켜야할 규칙입니다.

### 이슈 및 브랜치 규칙

- 이슈를 작성할 경우 자신이 할 일이 무엇인지 정확하고 자세히 정의하며, assignment를 통해 누가 할 역할인지 밝힙니다.
- 브랜치를 생성할 경우 Feature/#이슈번호, Release/#이슈번호로 생성합니다.

### 커밋 규칙

`init` : 초기화  
`feat` : 새로운 기능 추가  
`update`: 기능 수정  
`fix` : 버그 수정  
`docs` : 문서 수정  
`style` : 코드 포맷팅, 세미콜론 누락, 코드 변경이 없는 경우,  
`linting` design: 레이아웃 수정, UX 또는 UI에 대한 커밋
`refactor` : 코드 리팩터링  
`test` : 테스트 코드, 리팩터링 테스트 코드 추가  
`chore` : 빌드 업무 수정, 패키지 매니저 수정, 그 외 자잘한 수정에 대한 커밋

### 코드리뷰 가이드

1. `File change`에서 변경사항 확인
   1. 코드가 이해가 되지않으면, local에 clone하여 실행
2. `File change`에서 `Start a review`로 문제, 해결 방안, 리뷰 등 코멘트를 남깁니다.
   1. 확실한 개선 방향을 찾지 못한 경우, 3번을 진행한 이후, `conversation`을 통해 의견을 수렴합니다.
3. 모든 코멘트를 남긴 후, `Finish your review`에서 다음과 같은 피드백 종류를 선택하여 리뷰를 진행합니다.

   1. 일반적인 피드백을 주는 경우, `Comment`
   2. 이제 합쳐도 문제가 없을 경우, `Approve`
      - ⭐⭐⭐ **Approve의 조건:**
        - Sonarcloud 코드분석에서 문제가 없을 것
        - 단, `Code smell`에서 `Minor 등급의 문제`는 발생해도 approve가 허용됨!
   3. 확실히 수정하고 넘어가야할 문제인 경우, `Reqeust changes`

   `c` 해당한 리뷰를 한 경우, `Author`는 반드시 재 커밋을 하여야합니다.

4. 반영된 부분은 `Resolve conversation`을 하여 처리 완료됨을 표시합니다.
5. 리뷰를 마친 후, 코드가 더 수정되었다면 다시 재-리뷰를 요청할 수 있습니다.

### styled component 네이밍 규칙

### S-dot 네이밍

```jsx
<S.MainPageLayout>
	<S.HeaderTitle>메인 페이지</HeaderTitle>
  <S.HeaderNav>
      <S.HeaderNavList>
      	<S.HeaderNavItem>홈</S.HeaderNavItem>
      	<S.HeaderNavItem>메뉴1</S.HeaderNavItem>
      	<S.HeaderNavItem>메뉴2</S.HeaderNavItem>
      </S.HeaderNavList>
   </S.HeaderNav>
</S.MainPageLayout>
```

최상위 컴포넌트 명

- '컴포넌트명'Layout

각 태그들의 컴포넌트 명

- div : '컴포넌트명'Box
- section : '컴포넌트명'Section
- ul : '컴포넌트명'List
- li : '컴포넌트명'Item
- p : '컴포넌트명'Paragraph
- span : '컴포넌트명'Span

컴포넌트들을 묶어주는 컴포넌트 명

- '컴포넌트명'Row/Col
