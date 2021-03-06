Event types that appear in the browser
======================================
    form event: HTML 문서의 form element에 변화가 생기거나 submit 버튼을 누르는 경우 등의 상황에서 발생
    window event: 페이지가 모두 로드되었을 때 발생하는 onload event 등이 있음
    mouse event: 사용자가 마우스를 조작했을 때 발생
    key event: 사용자가 키보드를 조작했을 때 발생
#### Event
    click: mouser event로 HTML element를 마우스로 클릭한 경우 발생
    change: form event로 form element의 내용이 변경된 경우 발생
    keydown: key event로 key가 눌린 경우 발생하는 이벤트
    EventHandler에서 return false시 키 입력 비활성
    실제로는 keydown event -> keypress event -> keyup event 순으로 이벤트가 발생하며 keypress event 발생시에 키가 입력됨.
    keydown event 에서 return false를 한 경우 keypress event가 이어서 발생하지 않음
    submit: form 태그의 submit 이벤트
    EventHandler에서 return false시 브라우저 자체 기능(페이지 이동) 비활성
#### EventHandler 설정
-----------------------
##### HTML Tag의 속성으로 Event Handler 추가
    Tag의 속성에 event handler 코드를 추가
    onEvent 속성 사용(onclick, onchange, onkeydown...)
##### property에 직접 Handler 설정
    Element의 `"on"+"이벤트"`의 속성에 메소드를 직접 지정
```js
document.getElementById("form").onsubmit = function eventHandler() {
    console.log("from property");
    return false; // 브라우저의 submit 처리 비활성
}
```
#### addEventListner 메소드
    element의 addEventListener(이벤트, 함수) 메소드를 호출해, eventHandler 등록
    여러개의 이벤트 핸들러를 등록할 수 있음
```js
document.getElementById("form").addEventListener(
    "submit",
    function eventHandler() {
        console.log("from addEventListener")
        return false;
    }
)
```
#### removeEventListener 메소드
    element의 removeEventListener(이벤트, 함수) 메소드를 호출해, eventHandler 삭제