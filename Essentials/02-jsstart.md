# JavaScript

## 데이터 타입확인

### typeof
```javascript
console.log(typeof 'Hello World')  //string
console.log(typeof 123)  //number
console.log(typeof true)  //boolean
console.log(typeof undefined)  //undefined
console.log(typeof null)  //object
console.log(typeof {})  //object
console.log(typeof [])  //object
```

typeof라는 키워드로는 객체데이터와 배열 데이터를 정확하게 구분해서 확인하기 어렵다

그래서 하나의 함수를 만들어 type을 구분해볼 수 있다

### 함수
```javascript
function getType(data) {
  return Object.prototype.toString.call(data)
}
console.log(getType(123))
console.log(getType(true))
console.log(getType({}))
console.log(getType([]))
console.log(getType(null))
```
![alt text](assets/getType.png)

.slice(8, -1)을 붙여주면
```javascript
function getType(data) {
  return Object.prototype.toString.call(data).slice(8, -1)
}
```
![alt text](asstes/slice.png)