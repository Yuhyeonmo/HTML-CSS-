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

2. 사용자 지정 속성 (* IE에선 지원안됨 )
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

## DAY 6
### 요약
    1. 사용자 지정속성은 :element 으로 선언하고 var() 함수를 통해서 사용하여 나타낸다.
    2. before, after 는 요소앞뒤에 생성되는 자식 요소
    3. content 는 가상선택자 에 필수로 들어가야 하는 속성 / 값으로 none, img, string
    4. 토글이란 하나의 설정 값으로부터 다른 값으로 전환하는 것
    5. label 태그는 사용자 인터페이스 항목을 설명하는 데 사용. input 태그와 결합 시 클릭 영역을 확장해주는 다는 이점이 있음.
    6. Inline-block 은 inline 설정을 갖되, 높이와 너비를 지정할 수 있음.
    7. input 태그의 타입을 checkbox 로 지정한 태그에 :checked 를 사용하면 체크할 때 일어나는 스타일을 지정
    8. 일반 형제 결합자 ~ 는 두 선택자 사이 위치하며, 앞과 뒤의 선택자를 연결합니다.

    rem으로 크기 지정하기.
    rem 글꼴의 크기를 지정하는 단위로 px 절대단위 이지만, rem은 상대단위로 해상도에 따라 크기가 유동적으로변한다는 장점.

    overflow 속성
    visible 기본값 , 요소를 자르지 않으며 안쪽 여백 상자밖에서도 그릴 수 있음.
    hidden 밖에서 나타나는 값을 자름.
    scroll 요소가 넘치면 스크롤바를 띄워준다.
    auto 요소가 안에 들어가면 visible 동일하나 넘치면 스크롤

