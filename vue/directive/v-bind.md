v-bind
======
엘리먼트 속성을 바인딩
```html

<div id="app">
    <span v-bind:title="message">
        잠시 마우스를 올리면 동적으로 바인딩 된 title를 볼 수 있습니다.!
    </span>
</div>
<script src="https://unpkg.com/vue"></script></script>
<script>
    var app = new Vue({
        el: '#app',
        data: {
            message: '이 페이지는 ' + new Date() + ' 에 로드 되었습니다'
        }
    })
</script>
```