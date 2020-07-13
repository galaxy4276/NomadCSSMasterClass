# NOMAD CLASS CSS LAYOUT

### #1 FLEXBOX
* display: block 기본 속성을 가진 Element는 자신의 옆에 어떠한 대상도 올 수 없게 되어있다.
* flex 부모가 children 을 제어할 수 있다. body -> div -> div X, div -> div O
* row(열) -> 가로
* column(행) -> 세로
* flexBox는 아이템이 모두 같은 줄에 있도록 유지 함. -> 요소가 많아지면 너비를 조절함.

  #### axis, default value
  * main axis 의 기본 값은 row, -> flex-direction: row;
  * main axis 가로 일 때 cross axis 는 세로
* #### justify-content
* justify-content -> 수평 축에 있는 flex children 의 위치를 변경시켜 줌.
* space-between -> 박스 사이에 공간을 줌
* space-around -> 박스 주변 옆 공간을 같게 만들어 줌
  #### align-items
  * align-items 기본 값은 flex-start, flex-end -> end 부분에 요소를 배치하게 됨.
  * cross axis 방향으로 아이템을 옮길 때는 align-items 를 사용 ( main axis -> justify-coentent )
  * align-items[stretch] 는 전체 높이까지 쭉 뻗어진다.
  #### align-self
  * cross axis 에 해당하며 items 와 동일한 기능을 수행하지만 한 BOX에 해당된다.
  * 즉, 부모가 아닌 자식에게 할당하여 개개인에게 지정해줄 수 있는 명령이다.
  * order 순서를 결정하며 모든 요소의 기본 값은 0임을 유의
  #### align-content
  * line 을 제어함 ( cross axis )
  #### flex-wrap 
  * default no-wrap
  * wrap 옵션은 child의 크기를 유지하게 함.
  #### flex-grow, flex-shrink
  * child 에게 줄 수 있는 옵션
  * flex-shrink defalut 1
  * flex-shrink 는 wrap이 nowrap일 때 너비가 줄어드는 배수 값
  * flex-grow default 0
  * flex-grow 는 shrink 와 반대, box가 얼마나 커질 지
  * 1을 값으로 하였을 때 남아있는 빈 공간 만큼 커 짐 (최대)
  * responsive design 에 유용
  #### flex-basis
  * child 에 적용되는 property
  * element 에게 initial size 를 제공
  * flex-basis 는 main axis 에서 작동하기에 width 이다. 즉 flex-direction 이 column 값일 때 height가 되어버림.
  #### wrap
  * flex는 기본적으로 모든 것을 한줄에 두려고 한다.
  * flex-wrap: wrap 설정 시 여러 줄에 걸쳐서 표현한다.
  #### flex-flow
  * flex-direction, flex-wrap 을 동시에 수행함.
  
### GRID
* GRID 디자인은 father에서 해야함.
* grid 라인은 음수로 카운트할 수 있음 ( ex -1 은 마지막 라인 )
* https://studiomeal.com/archives/533 grid 정리 표 
* content: 전체 grid 표를 의미함.
* grid 는 기본적으로 100% 크기를 지님.
* 그리드 자주 사용 프로퍼티: start, center, end
  #### column-gap 
  * 컬럼간의 간격을 말함
  #### row-gap
  #### gap
  * column, row  all gap
  #### repeat
  * grid가 지니고 있는 함수
  * 1 arg: 반복할 횟수, 2 arg: 크기
  #### grid-template-areas
  * 눈에 잘보이게 layout을 디자인함.
  #### grid-area
  * grid 이름변수를 적용
  #### grid-column-start, grid-column-end
  * 컬럼이아닌 line을 뜻함.
  * start: 1, end: 2 일시 line 1에서 2까지
  * span = 시작 과 끝 을 의미함. cell 갯수를 적어준다.
  #### fraction (fr)
  * 사용 가능한 공간을 뜻함.
  * 비율로 계산한다.
  #### grid-template
  * 이름을 부여할 때 모두 붙이던가, 붙이질 말아야함.
  * row 정의 후 / 각 column 사이즈 정의
  * repeat 함수가 적용되지 않음.
  #### justify-items
  * main axis 수평 부분
  * 기본값은 stretch
  * property: start, end, center, stretch(default)
  #### justify-content
  * grid 전체를 제어
  * start, center, end, space-around 등등 프로퍼티 존재 + space-evenly
  #### align-items 
  * cross axis 수직 부분
  * cell 중에 하나, 즉 한 칸의 아이템
  #### align-self, justify-self, place-selft
  * 개별 cell을 컨트롤
  #### place-items
  * 기본형식 y / x; ( except /)
  #### align-content
  #### place-content
  * align-content, justify-content
 
  #### grid-auto-rows, grid-auto-column
  * 추가되는 열, 행에 대해 자동적으로 생성해주는 옵션
  #### grid-auto-flows
  * 추가되는 열에 대해 column을 생성할 지 row를 생성할 지 결정할 수 있음.


  #### minmax()
  * 크기의 최소, 최대 크기를 지정한다.
  예) 1fr 일 경우 공간에 따른 제약을 없애기위해 최소사이즈 100px, 1fr 지정 가능


  #### auto-fill, auto-fit
  * column을 가능한 한 많이 만들어줌.
  * auto-fill은 화면에 element 갯수만큼 그려줌
  * auto-fit 은 화면에 꽉차게 그려줌