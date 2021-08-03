# HTML-CSS-
30일 챌린지 - 책을 통한 학습
## DAY 1 - Web, HTML
1. WEB
- 네트워크 : 컴퓨터 - 컴퓨터를 연결하는 망
- 인터넷 : 이러한 망들의 모임
- 웹은 인터넷으로 연결된 사용자들이 정보를 공유할 수 있는 서비스

2. HTML
- 하이퍼텍스틀 마크업하는 언어를 의미함.
    + 정해진 순서없이 참조를 통해 한 문서에서 다른 문서로 접근

3. 웹사이트 
- URL 기반으로 인터넷에서 서비스되는 웹페이지 집합

* VS Code 확장프로그램 6가지 
+ Auto Close tag
+ Html snippet
+ Live server
+ Material Icon
+ Prettier
+ korean(한국어패치)

## DAY 2 - CSS
1. CSS는 Cascading Style Sheets 의 약자로 사용자에게 보여지는 페이지를 꾸밈.
2. font-size 글씨 크기 조정, text-align(left, right, center, justify)
3. CSS 선택자는 5가지 유형
- 전체선택자(*) 모든 HTML 문서를 선택해 스타일 적용
- 유형 태그 선택자는 특정 유형(태그)를 지정해 작성하는 방식으로 타입 셀렉터라고도 합니다.
- ID 선택자는 해당 태그의 고유한 이름에 따라 스타일을 적용합니다.
- 클래스 선택자는 class의 요소를 지정하는 선택자입니다.
- 복합 선택자는 서로의 관계와 위치를 유용하게 결합하는 방식을 제공.

블록레벨, 인라인 레벨
블록레벨 요소는 가로 줄 전체를 차지, 인라인 레벨요소는 요소가 있는 공간만 차지합니다.
display : 속성을 통해 바꿔줄 수 있다.

박스모델 : 마진(margin), 테두리(border), 패딩(padding)

플렉스박스 특징 (꼭 부모 태그를 선택자로 지정)
1. 공간에 맞추기 : display flex
2. 주축 정렬
3. 교차축 정렬

## DAY 3 
1. 가상선택자
가상선택자는 두 가지 분류
동적 가상 클래스
구조적 가상 클래스
- 동적 가상 클래스
동적 가상 클래스는 어떤 상태나 조건이 발생할 때, 사용자의 액션에 따라 스타일이 바뀌는 선택자

- 구조적 가상 클래스
구조적 가상 클래스는 CSS 에서 id, class 등의 선택자를 사용하지 않고 요소를 선택할 수 있습니다.
first-child, last-child, nth-of-type, only-of-type

## DAY 4 ~ 5

1. Box Layout - Header main (nav, article) footer
- display : flex , justify-content, align-items 는 정렬 대상의 부모
- align-item 부모의 높이가 정해졌는 지 확인.

2. 사용자 지정 속성
var(사용자지정속성);
```HTML
<style>
    :root {
        --title-color : red;
    }
    h1 {
        color : var(--title-color);
    }
</style>
<body>
    <h1>test</h1>
</body>
```

before, after 는 가상선택자를 사용할 때 반드시 content를 써야한다.
none
string 
img

```HTML
<style>
    .box {
        width : 400px;
        height : 100px;
        background-color : blueviolet;
        position : relative;
    }

    .box::after {
        content : "";
        width : 400px;
        height : 100px;
        top : 100px;
        background-color : brown;
        position : absolute;
    }
</style>
<body>
    <div class="box"></div>
</body>
```

체크박스 선택자
체크박스(input type="checkbox") ::checked