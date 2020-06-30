
# 코딩과제 관련 수행하며 배운 점

### inline-block 50% 두 개 일 때 100% 초과하는 이슈
inline-block은 html의 white-space를 고려한다. 만약 두 div를 붙여놓는다면 딱 100%가 될 것. 하지만 나는 html의 가독성을 위해 각기 margin-right: -4px; 처리를 줬다.

### flex-flow: column wrap;
요소들이 밑으로 흐르고 height보다 내용물이 길어지면 새로운 column을 만든다. 지금 와서 깨달은 거. max-height로 했으면 부자연스러운 공백이 없었을 텐데 아 너무 아쉽다. 왜 그 때는 생각 못 했지? 그래도 이걸로 엄청 고생했는데 masonry를 css로만 구현하는 데 성공해서 너무 뿌듯했다. 처음에는 부트스트랩 그리드 시스템 살리려고도 노력했고 float로도 해보려고 했고 grid도 시도했는데. css는 어려워지려면 한도 끝도 어려워질 수 있다는 걸 절감.

### IE 크로스 브라우징
_:-ms-fullscreen, :root 이거 넣으면 IE11에서 된다. 또 미디어쿼리로도 뭐 넣으면은 된다. 근데 환장 포인트는 그 반응형이랑은 동시에 절대 안 먹는다. 그래서 결국 !important 처리했다. 왠지 엄청 싫어하실 것 같은 기분이 들었지만 이게 제일 깔끔한 처리였단 말이여.ㅠㅠ

# 코딩과제 관련 기존 코드에서 배운 점

### meta tag

#### http-equiv 속성
content 속성도 함께 명시해야만 한다.  
content 속성에 명시된 값에 대한 HTTP 헤더 제공.  
X-UA-Compatible일 때는 어떤 렌더링 엔진을 사용할 것인지 전달 가능.  
실험적 프로젝트가 아닌 이상 IE=Edge 권장됨.

#### og
페이스북의 오픈그래프 프로토콜을 사용하는 태그. 사용자 클릭 전에 미리 해당 웹사이트를 크롤러가 방문하여 HTML head의 메타 데이터를 크롤링하며 미리보기 화면을 생성한다. (아 이게 이거구나 쨍그랑 대박쓰)

#### format-detection
content에 telephone=no를 입력하면 전화 번호 모든 자동 서식이 제거된다.

### normalize.css 와 reset.css
1. normalize는 스타일을 전체 해제하기보다는 유용한 디폴트들을 남겨둔다.
2. normalize는 reset는 커버하지 못하는 흔한 버그들을 고쳐준다.
3. normalize는 데브툴을 어지럽게 만들지 않는다.
4. normalize는 더 모듈화되어 있다.
5. normalize는 문서화가 더 잘 되어 있다.
6. 제로에서부터 시작하지 않기 때문에 코드를 더 적게 쓰게 된다.  
(Thank you stackoverflow! At least I tranlated it myself)

### flex

#### flex 속성
flex-grow, flex-shrink, flex-basis의 단축 속성.  
flex-basis는 flex item의 초기 크기 지정.

### 웹 접근성

#### 애니메이션
@media screen and (prefers-reduced-motion:reduce) 안에 none 선언 하면 애니메이션 축소 기능 설정한 유저에게 끌 수 있음.

### 이미지 처리
배경을 figure로 처리한 게 인상적.