### BOX MODEL과 FLEX MODEL
</br>

***box용어 정리*** <br>
flex box : flexible box <br>
flex box layout : 아이템이 배열된 방향을 정할 수 있다 = 주축 (main axis) <br>
cross axis : 주축과 수직한 축 <br>
border : 테두리 </br>
padding : 보충재, 즉 content와 border사이의 간격 </br>
margin : 요소 간의 여백, 즉 border로부터 다른 content 사이의 여백 </br>
**블록 레벨 요소** : 한 줄을 차지하는 박스 </br>
- 부모요소의 한칸 한칸을 차지한다
- 부모요소의 전체공간을 차지한다 </br>

**인라인 레벨 요소** : 자신만을 감싸는 박스 </br>
- 자신이 소유한 것만 감싼다
- 부모요소의 전체공간을 차지하지 않는다 </br>

<br>
<br>


***flex box 속성 정리*** <br>
1. flex **container(부모)** 속성: flex-direction, flex-wrap, justify-content, align-items, align-content <br>
2. flex **item(자식)** 속성: flex, flex-grow, flex-shrink, flex-basis, order

<br>
<br>

**justify-content**
- flex item을 **main axis**를 기준으로 어떻게 정렬할지를 결정
- 기본값은 flex-start인데, flex item을 main axis의 맨 앞으로 정렬
- 속성값으로는 flex-end, center, space-between, space-evenly, space-around 등을 사용 <br>

**align item**
- flex item을 cross axis를 기준으로 어떻게 정렬할지를 결정
- 기본값은 stretch인데, flex item을 flex container의 높이 또는 너비만큼 늘려준다
- 속성값으로는 center, flex-start, flex-end, baseline 등을 사용