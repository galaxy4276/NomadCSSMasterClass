# NOMAD CLASS CSS LAYOUT

### #1 FLEXBOX
* display: block 기본 속성을 가진 Element는 자신의 옆에 어떠한 대상도 올 수 없게 되어있다.
* flex 부모가 children 을 제어할 수 있다. body -> div -> div X, div -> div O
* row(열) -> 가로
* column(행) -> 세로
* justify-content -> 수평 축에 있는 flex children 의 위치를 변경시켜 줌.
* space-between -> 박스 사이에 공간을 줌
* space-around -> 박스 주변 옆 공간을 같게 만들어 줌
  #### axis, default value
  * main axis 의 기본 값은 row, -> flex-direction: row;
  * main axis 가로 일 때 cross axis 는 세로
  #### align-items
  * align-items 기본 값은 flex-start, flex-end -> end 부분에 요소를 배치하게 됨.
  * cross axis 방향으로 아이템을 옮길 때는 align-items 를 사용 ( main axis -> justify-coentent )
  * align-items[stretch] 는 전체 높이까지 쭉 뻗어진다.
