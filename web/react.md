# REACT

리엑트 = 사용자 정의 태그를 만드는 기술  
사용자 정의 태그를 선언 할때는 무조건 처음 문자가 대문자여야함  
리엑트 사용자 정의 태그 = 컴포넌트  
  
사용자와 상호작용할때 컴포넌트에 동적인 값을 집어 넣어야할 때에는 상태를 사용하여야함  
상태 = 동적인 값  
   
props = 외부에서 내부에게 주는 데이터  
useState = 상태로 만드는 함수  
const [변수이름,함수이름] = useState("'')  
상태 값 읽을땐  변수 사용  
상태 값을 변경할땐 함수(set변수이름)를 사용  
  
상태에 추가 데이터를 넣는 경우  
원시 데이터인 경우 => 원래 데이터를 사용해도 됨  
객체 데이터인 경우(객체,배열) => 복사된 데이터를 사용해야함  
예) const [value,setValue] = useState([1]);  
    x&nbsp;&nbsp;value.push(2);  &nbsp;&nbsp;  o &nbsp;newValue = [...value];  
&nbsp;&nbsp;&nbsp; setValue(value);&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; newValue.push(2);  
&nbsp;&nbsp;&nbsp; setValue(newValue);  
이유: 기존 데이터와 새로운 데이터가 같다면 렌더링 해주지 않기 때문  
  public = 정적인 리소스들을 모아놓은 폴더
src = 소스 코드 파일들을 모아놓은 폴더
package.json = 모듈 정보를 json 형태로 모아놓은 파일
node_modules = 설치 모듈들이 모인 폴더


babel이란 컴파일러를 통해 jsx-> js로 변환  
react 사용시 무조건 부모 요소로 감싸야하는데 이때 무슨 태그도  사용하고 싶지 않다면 빈 태그로 감싸면됨  
빈태그는 Fragment라고 부름  
jsx에서 js 사용시 중괄호로 감싸야함  
  
State Batch처리   
이벤트 핸들러 함수 내 state 변경 요청을 모아 일괄적으로 한번에 업데이트함  
예) state 내부(number = 0) =>   
setNumber(number + 1);   
console.log(number);  
콘솔: 0  
업데이트 하기 전 number가 찍힘  

  ---
  # 라이브러리
React Routing  
리액트에서 사용자가 요청한 URL에 따라 해당 URL에 맞는 페이지를 보여주는 컴포넌트가 있는 라이브러리  
  
Routes = Route 컴포넌트를 감싸 규칙이 일치하는 라우트를 찾아 렌더링 시켜주는 컴포넌트  
Route = path 설정과 이 path에서 사용할 컴포넌트를 설정 하는 컴포넌트  
Link = a 태그 처럼 링크를 바꿔주지만 페이지를 새로 불러오는게 아닌 브라우저 주소의 경로만 바꾸는 기능을 하는 컴포넌트  
styled-components  
css나 scss파일이 아닌 js로 만든 컴포넌트에 바로 삽입하는 스타일 기법  
styled 함수 = css를 적용시키는 컴포넌트를 만들 수 있음  
예)  
const StyledButton = styled.button`  
  padding: 6px 12px;  
  border-radius: 8px;  
  font-size: 1rem;  
  line-height: 1.5;  
  border: 1px solid lightgray;  
  color: gray;  
  background: white;  
`;  
function app() {  
  return <StyledButton>버튼</StyledButton>;  
}  
  
styled-components를 사용하는 이유(CSS-in-JS)  
js 환경을 최대로 활용 할 수 있음  
내가 사용하고 있는 스타일만 DOM에 포함 시킴    
글로벌 네이밍을 신경쓰지 않아도 됨  
기존 css보다 편의성과 확장성이 높음 (props를 전달받아 css 속성값으로 활용)  
  
#  리덕스

상태값을, component 에 종속시키지 않고, 상태 관리를 component 바깥에서 관리 하는 것

redux 를 적용할 시 스토어가 생김 스토어 안에는 프로젝트 상태에 관한 데이터가 있음

작동 방식

component 가 store에 접근
이후 state 값이 변경될 시 dispatch()가 상태를 변경해 달라고 Store에 요청(dispatch() 내부에는 액션을 반드시 담아야함) 
action 함수에는 type, payload 등을 담음
값을 전달 받은 Store는 Store 내부 Reducer 함수를 통해 상태를 변경함.
Reducer는 변경 전 상태와 action 객체를 인자로 받고 새로운 상태를 뱉음.
Store는 변경된 상태를 받아 기존 상태를 변경된 상태로 갈아 끼움  
상태변경이 끝나면 상태변경을 요청한 컴포넌트에 상태가 변경되었음을 알림.
해당 컴포넌트 리렌더링.

combineReducers 리덕스 합치기
connect(mapStateToProps, mapDispatchToProps)(TodosContainer) component 연결 하고 상태 확인
useSelector() 상태 변경 확인
createAction 액션 생성
handleActions 액션에 따라 함수 호출

리액트 프로젝트에서 리덕스를 사용하면 업데이트에 관련된 로직을 리액트 컴포넌트에서 완벽하게 분리시킬 수 있으므로 유지 보수성이 높은 코드를 작성해 낼 수 있다.
규모가 큰 프로젝트에 리덕스를 적용하면 상태를 더 체계적으로 관리할 수 있다.
npm create-react-app . 현재 디렉토리에 리엑트 설치    
npm start 실행    
npm run build 배포하기 좋은 형태로 파일 변환    
npm i styled-components    
npm i react-router-dom  