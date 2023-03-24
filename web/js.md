# js 공부하면서 막 적어 놓는 곳

## js와 html
```
html에서 js를 연결할 시 document라는 객체에 html에 정보가 들어감.
document = 하나에 객체기 때문에 자바스크립트를 통해 접근하여 변경할 수 있음.
예를 들어 document.querySelector('h1') 사용시 document란 객체에 들어 있는 h1 요소에 접근함.
또한 js도 css처럼 html을 명령어를 통해 스타일을 변경할 수 있음.
하지만 js와 css에 역할을 명확히 하는 것이 좋기 때문에 최대한 사용하지 않는 것이 좋음.
```
## js에서의 객체
```
값 또는 기능을 가지고 있는 데이터(document,window 등) 
객체가 가진 기능을 메서드라고 함.
```
## " ` " 이건 뭐야?
```
\`문자열 ${data}`  문자열 표기법으로 변수나 연산 등을 삽입할 수 있음.
```

## null 과 undefined의 차이
```
null = 값이 비었다,undefined = 아직 정의 되지 않았다.
```
## function() 와 function
```
()가 있는 경우 함수가 바로 실행됨 그러나 ()가 없으면 따로 실행 시켜줘야 함.
그래서 보통 이벤트를 실행 할때 ()를 쓰지 않고 사용하여 특정 이벤트 발동될 때 실행 시킴.
 ```
## localstorage와 cookie
```
localstroage란 데이터 임시 저장소로 브라우저 자체에 작은 데이터를 저장해 놓을 수 있는 방법임.
cookie 또한 데이터 임시 저장소로 브라우저에 데이터를 저장하는 방식임.
예로 로그인 유지같은게 있음.
두 개의 차이 
1.저장 할 수 있는 데이터 양: cookie(4KB) < localstorage(5MB)
2.저장 방식: localstorage = 로컬 cookie = 서버,로컬
```
## 변수 선언
```
js에 경우 알아서 자료형 타입을 지정해 주기 때문에 변수 선언 방법은 var,let,const만 있음.
var = 전역 변수
let = 지역 변수
const = 상수
var을 사용하면 유지보수가 힘들어 이제는 잘 사용되지 않음.
let 또한 보안 상에 문제가 있을 수 있기 때문에 변경이 이뤄져야하는 데이터가 아니라면 사용하지 않음.
중복되는 데이터는 const를 사용하여 상수로 지정해 주는 것이 좋음.
```
## array,object
```
array는 여러 변수를 한 곳에 저장 할 수 있는 방식
object도 여러 변수를 한 곳에 저장 할 수 있는 것은 똑같지만 선언할때 더 자세하게 지정할 수 있음.
선언 방식 예시
array: const playerArray = ["nico",121212,false,"little bit"];
object: const player = {
   		                name : "Yeojun",
    		            points : 121212,
    		            handsome : false,
    		            fat : "liitle bit"
	  	               };
사용 방법 예시
array: playerArray[0]
object: player.name
```
## className과 classList의 차이
```
className같은 경우 Element에 모든 클래스를 끌고 오지만 classList는 특정 class만을 지정 할 수 있음.
```
## 배운 명령어(중요하다고 생각 하는 것들)
```
document.querySelector("Element"); = css처럼 특정 요소를 지정하여 접근 할 수 있음.
Element.addEventListner("event",function) = 지정한 이벤트를 하면 함수 실행.
Element.classList.toggle("classname"); = 지정한 클래스가 있으면 없에주고 없으면 생성해줌.
document.createElement("Element") 지정된 이름의 html 요소를 만들어 반환
Node.appendChild("Node") 노드 밑에 지정한 자식 노드 추가
```