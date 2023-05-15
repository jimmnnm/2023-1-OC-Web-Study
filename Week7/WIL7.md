## Youtube Clone Coding <br>
1. view 안에 header와 container가 flex-direction:columns 방향으로 배치 <br>
2. container안에 main-container와 aside-container가 row방향으로 배치 <br>
3. container안에 3개의 container가 columns 방향으로 배치 <br>
4. video-info-container안에 정보들이 columns 방향으로 배치 <br>
5. comment-container안에 댓글들이 columns 방향으로 배치 <br>
6. header안에 button들 row방향으로 배치 <br>
<br>
<br>

### ! html 코드작성 <br>
class 선택자 활용 - 공통된 요소들을 묶음으로 만들고, 이름을 붙여주어 재활용<br>
- class = "grey-bakcground" : 아이콘에 	커서를 올렸을 시 회색 배경 변환 목적<br>
- id = "header" : header뿐만 아니라 각 요소들이 중복이 아니기 때문에 id로 설정<br>
<br>
<br>

### ! 외부 style.css 코드 작성<br>
> **header** <br>
- 항상 top에 존재 + 휠을 내려도 고정 : top : 0; position : sticky;<br>
- 배경은 하얀색, 각 아이콘에 여백 존재<br>
- item이 row 방향으로 일정한 간격으로 존재 + 재활용: justify-content: space-between 클래스 작성<br>
>> . flex-row-space-between<br>
- row방향 배치<br>
- 일정한 여백 존재<br>
- 중앙선에 배치 <br>
>> . grey-background<br>
- 요소끼리 너무 밀착 X : margin<br>
- 요소의 테두리와 내용물이 너무 밀착 X : padding<br>
- 커서 접근 시 배경이 동그란 모양의 회색으로 변환<br>
- 커서가 손가락 모양으로 변환 : flex-row-center <br>
<br>

> **search_bar** <br>
- 테두리가 둥글고 긴 타원형<br>
- 입력창과 검색 버튼이 테두리와 약간의 거리 O : padding<br>
- 입력창과 검색 버튼이 flex row 방향 배치<br>
<br>

> **container** <br>
- main-container와 aside-container가 row 방향 배치 <br>
- main-container는 3가지 세부 컨테이너를 column 방향 배치 <br>

<br>
<br>
<br>


### ! 실습하면서 미흡했던 부분 코드<br>
```
.flex-column {
  display: flex;
  flex-direction: column;
  align-items: center;
}
```
<br>

```
.comment-box {
  display: flex;
  flex-direction: row;
  margin: 10px;
}

.comment-text-area {
  display: flex;
  flex-direction: column;
}

.comment-input-box {
  display: flex;
  flex-direction: row;
  margin: 10px;
  align-items: center;
}
```
<br>

```
.like-hate-area {
  display: flex;
  flex-direction: row;
}

.grey-button {
  background-color: whitesmoke;
  border-radius: 25px;
  padding: 15px;
  margin: 10px;
}

.grey-button:hover {
  background-color: lightgray;
  cursor: pointer;
}
```
<br>

**실습 실패 이유** <br>
- video-info 부분의 각 아이템을 grey-button으로 만들어야 하는 부분을 빼먹었다.. <br>
<br>
<br>

## ! 과제 <br>

id="container"에 main, aside container를 **row 방향**으로 묶고, main container에 실습 때 작성한 "video-info-container", "comment-container"를 넣고, **추가로 "video" 코드를 작성**하여 main container를 완성하였다.<br> 실습 시에 "comment-container"는 비워두어도 된다고 하셨는데 이를 비워두면 댓글들이 center에만 모이는 문제가 생겨서 **flex-start기능을 넣어** 박스를 채웠다. <br> 
```
#comment-container {
    width: 70vw;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
}
```
<br>

aside-container를 구현하는 것은 comment를 구현하는 방식을 참고하였으며 profile대신 thumbnail을 만든 것 빼고는 수월하게 진행할 수 있었다. <br>
<br>
## ! 과제 코드 (style.css) <br>
```
#aside-container {
    width: 30vw;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
}

.video-thumbnail-box {
    display: flex;
    flex-direction: row;
    margin: 5px;
}

.video-thumbnail {
    width: 100px;
    height: 100px;
    margin: 5px;
}

.video {
    width: 500px;
    height: 500px;
    margin: 5px;
}
```
<br>

*참고 문헌*

https://oneroomtable.tistory.com/entry/flex-%EC%86%8D%EC%84%B1-%EC%82%AC%EC%9A%A9-%EB%B0%A9%EB%B2%95-%EC%A2%8C%EC%B8%A1-%EC%9A%B0%EC%B8%A1-%EC%A4%91%EC%95%99-%EC%A0%95%EB%A0%AC-%EB%93%B1#gsc.tab=0 <br>

https://studiomeal.com/archives/197 <br>
