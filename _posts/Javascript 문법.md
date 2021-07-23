# Day 1

# 기본형과 참조형

- 기본형
객체가 아닌 데이터 유형
예시로 Number,String,Boolean,Symbol,null,undefined

    ⇒ 값을 그대로 할당하는 것.
    ⇒ 메모리상에 고정된 크기로 저장되며 원시 데이터 값 자체를 보관, 불변적

    ```jsx
    let num = 4;
    let flag = false;
    let name = 'jin-Pro';
    ```

- 참조형

    기본형 데이터의 집합을 참조형이라 한다.
    예시로 Object,Array,Function,Map..

    ⇒ 참조형 데이터는 값이 지정된 주소값을 할당한다.
    ⇒ 변수에 할당할때 값이 아닌 데이터의 주소를 저장한다.

    ```jsx
    let jinPro = {
    	name : '김영진',
    	age : 25,
    }

    let dog = ['제니','금비']
    ```

# 얕은 복사와 깊은 복사

- 참조형은 데이터의 주소를 저장하기때문에
얕은 복사를 하게 되면 데이터의 주소를 같이 가리키게된다.

따라서, 데이터의 주소가 가리키는 데이터가 바뀌게된다면
얕은복사를 한 두 참조형 모두 값이 변한다.

즉, 두 참조형이 다르게 작동이 되길 원한다면, 깊은 복사를 하여야한다.

새로운 참조형을 만들어서 값을 넣어주는것이 편리하다고 생각하여.
배열의 경우 forEach를 사용하여 모든 item값들을 push한다.

```jsx
let firstArray = [1,2,3,4]
let secondArray = firstArray   // 같은 주소값을 참조함

secondArray[0] = 3
console.log(firstArray[0])   // 1이 아닌 3이 출력된다.

let thirdArray = [...firstArray]
thirdArray[0] = 1

console.log(thirdArray[0])   // 1
console.log(firstArray[0])   // 3
```

---

## **Sort()**

- arrayobj.sort(sortFunction)에 sortFunction을 생략한다면 오름차순,ASCII 문자 순서로 정렬이된다.   즉, 문자열 정렬을 원한다면 sortFunction을 비워두고 sort()를 사용하는 것이다.

```jsx
let stringArray = ['a','c','b']

stringArray.sort()

console.log(stringArray)   // ['a','b','c']
```

- 정수형 정렬의 경우 sortFunction을 비워두게 된다면 입력된 숫자값을 아스키코드값으로 변환하여 정렬을 하기 때문에, sortFunction을 목적에 맞게 구현을 해주어야한다.

```jsx
let numberArray = [4,3,2,1]

numberArray.sort(function(a,b){
	return a-b;
})

console.log(numberArray)  // [1,2,3,4]
```

## VSCode 단축키

- ctrl + b   : 메뉴 창 토글
- ctrl + j    : 터미널 토글
- Alt + ←  : 이전 작업한 라인으로 이동
- ctrl + d  : 특정 문자탐색
- fn + →   : 라인 맨 끝으로 이동

- `JavaScript 문법`

    [배열](https://www.notion.so/682f234ce15d4405aead424824191ce8)

    [객체](https://www.notion.so/cefbef9e4dcc4049895a24120d0f725d)

    [클래스](https://www.notion.so/cec57de822ae44aabfb918b4df2ed019)

    [비구조화 할당](https://www.notion.so/a7d0dcd2c6de47e885e0514b8cb901ff)

    [spread와 rest](https://www.notion.so/spread-rest-97ab87230cba4d82bd41804b7e96c525)

[Git](https://www.notion.so/Git-5ac9f19dd80a42e9ac355ce48f6d443e)