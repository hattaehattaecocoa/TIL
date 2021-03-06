배열
====
> 값을 저장할 수 있는 엘리먼트(변수)의 연속된 공간. 주소(인덱스.index)를 이용해 각 엘리먼트에 접근 가능  
> 배열은 비슷한 객체나 값을 여거 개 관리해야 할 때 유용하고, 객체는 속성이 여러 개인 복잡한 데이터 타입이 필요할 때 유용.ex) 연락처는 객체, 주소록은 배열
### 배열의 정의
+ 빈 배열 : `var arr = [];`
+ 초기화된 배열 : `var arr = [1, 2, 3, 4, 5];`
+ 엘리먼트에는 어떤 자료형이든 저장 가능
    - `var mixed_arr = [1, true, 3.14, "string", {name:"object"}, [1,2,3]];`
+ 문자열 사용 방법과 비슷
### 배열의 길이
+ `.length` 속성 이용
### 배열의 엘리먼트에 접근하기
> 인덱스를 사용해서 각 엘리먼트에 접근
+ 대괄호 안에 인덱스를 사용 : `arr[index]`
    - `arr[0] = 1`
    - `console.log( arr[arr.length -1]);`
### 배열에 엘리먼트 추가/삭제
기본적으로 배열의 앞과 뒤에서 엘리먼트를 추가하거나 삭제 가능
+ `.pop()` : 배열의 뒤에서 엘리먼트 삭제하고 삭제된 값 리턴
    ```js
    var arr = [1,2,3,4,5];
    > arr.pop();
    < 5
    > arr;
    < [1,2,3,4];
    ```
+ `.shift()` : 배열의 앞에서 엘리먼트 삭제하고 삭제된 값 리턴
    ```js
    > arr.shift();
    < 1
    > arr;
    < [2,3,4];
    ```
+ `.push(element)` : 배열의 뒤에 엘리먼트 추가하고 배열 길이 리턴
    ```js
    > arr.push(6);
    < 4
    > arr;
    < [2,3,4,6];
    ```
+ `.unshift(element)` : 배열의 앞에 엘리먼트 추가히거 배열 길이 리턴
    ```js
    > arr.unshift(0);
    < 5
    > arr;
    < [0,2,3,4,6]
    ```
### 배열 뒤집기, 정렬
+ `.reverse()`
    ```js
    > arr.reverse();
    < [6,4,3,2,0]
    ```
+ `.sort()` : 오름차순으로 정렬
    ```js
    > arr.sort();
    > [0,2,3,4,6]
    ```
### 배열 붙이기, 검색하기
+ `arr1.concat(arr2)` : `arr1`과 `arr2` 붙이기
    ```js
    var arr1 = [1,2,3];
    var arr2 = [4,5,6];
    > arr1.concat(arr2);
    < [1,2,3,4,5,6];
    > arr1;
    < [1,2,3]
    > arr2;
    < [4,5,6]
    var arr3 = arr1.concat(arr2);
    > arr3;
    < [1,2,3,4,5,6]
    ```
    - `concat()`, `push()` 명령어 차이
        ```js
        > arr1.concat(arr2);
        < [1,2,3,4,5,6]
        > arr1.push(arr2);
        < [1,2,3,[4,5,6]]
        ```
+ `arr.indexOf(element)` : `arr`에서 `element`가 있는 첫 위치를 검색
    ```js
    var arr4 = [1,2,3,1,2,3];
    > arr4.indexOf(2);
    < 1
    ```
+ `arr.lastIndexOf(element)` : `arr`에서 `element`가 있는 마지막 위치를 검색
    ```js
    > arr4.lastIndexOf(2);
    < 4
    ```
### 문자열 split
문자열을 `구분자(separator)`로 나눠서 각각을 담은 배열을 반환하는 함수
```js
var str = "1,2,3,4,5";
arr = str.split(",");
arr = ["1", "2", "3", "4", "5"];

> "1-2-3-4-5".split("-");
< ["1", "2", "3", "4", "5"]

> "1a2a3a4a5a".split("a");
< ["1", "2", "3", "4", "5"]

> "1,2,3,4,5".split(",");
< ["1", "2", "3", "4", "5"]
```