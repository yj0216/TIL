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
  
npm create-react-app . 현재 디렉토리에 리엑트 설치  
npm start 실행  
npm run build 배포하기 좋은 형태로 파일 변환  