JavaScript
==========
+ 자바스크립트는 로직을 통해 문서의 구조와 스타일에 변화를 준다
+ 브라우저에서는 자바스크립트에서 HTML과 CSS에 접근할 수 있는 API를 제공 한다
### 스크립트 위치에 따른 실행
+ 브라우저는 HTML 문서를 읽으면서 script tag를 실행한다
    - HTML 문서 Element 파싱 보다 스크립트가 먼저 실행되면 접근되지 않는다
    - 페이지의 상단의 script에서 이후 파싱 될 Element에 접근하고 싶다면 onload등의 eventhandler로 실행되도록 해야 한다
+ async, defer 속성을 이용하면 스크립트의 실행과 문서의 로딩을 동시에 진행할 수 있다(비동기)