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