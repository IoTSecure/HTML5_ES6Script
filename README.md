# HTML5 문법
##### <> : 태그의 시작을 표시하는 기호. 밑에 나오는 설명들은 다 태그를 붙여야 함.
##### </> : 태그의 마지막을 표시하는 기호. 사용하지 않는 태그도 있음.

=========================

## !DOCTYPE html
### - 문서 형식 표시

## head, /head
### - 홈페이지에 필요한 문법들을 미리 로딩하거나 설명할 때 사용(탭 위에 마우스 가져다 놓으면 나오는 설명들을 여기에 설정함.)

### - 대표적으로 들어가는 요소들
1. meta charset = "utf-8" : meta 태그는 홈페이지의 설명을 담당함. 이 예제는 홈페이지의 인코딩 방식을 정의함.
2. title, /title : 탭에 뜨는 페이지 이름을 설정함.
3. link, /link : css 요소를 불러옴.
4. style, /style : css 요소를 바로 선언함.
5. script language = "javascript" type ="text/javascript" (ES6 스크립트) /script : javascript 요소를 사용함.
6. noscript (문장) /noscript : 사용자가 스크립트 제한을 했을 때 화면에 나타내주는 태그.
7. base href="(도메인)" target="_blank : <a>태그가 비었을 때 기본으로 사용하는 태그.

## body, /body
### - 홈페이지에 보여질 것들을 설정할 때 샤용.

### - 대표적으로 들어가는 요소들 (중요!)
1. div class="(설명)" (제목) /div : 컴퓨터의 폴더라고 생각하면 편함. 제목이 홈페이지에 보임.
2. ***h1, /h1, ... , h6, /h6 : 글자의 크기를 표현. 숫자가 높을 수록 크기가 작음.
3. ***hr : 줄바꿈.
4. ***p, /p : 문장을 표시함.
5. a href="(도메인)" (문장) /a : 하이퍼링크. p 태그 내부에 선언할 수 있음.
6. ul, /ul : 점으로 분리해 문장을 설명함.
7. ol, /ol : 번호대로 분리해 문장을 설명함.
8. li, /li : ul 와  ol  태그 내부에 선언함. 보일 아이템을 선언한다.
9. br : '\n'과 동일한 태그.
10. iframe src="(도메인)" title="(설명)", /iframe : 조그만 창에 도메인을 불러오고, 설명하는 태그.


# JavaScript (ES6Script)
- ES6의 중요부분만 다룹니다.

## 변수
1. var, let
- var은 전역변수, let은 C, C++의 for(int i = 1; i < n, i++)에서의 i (지역변수라 하나?).
2. const
-변경 불가능한 변수 선언할 떄 사용함. 그 외에는 let 과 같은 기능을 수행한다.

## 문자열
- 예제로 표현한다.
<br> let name = 'David';
<br> let msg = `Welcome ${name}!`;
<br> console.log(msg);
<br> 결과 : Welcome David!

## 반복문
- 예시로 표현한다.
1. for .. in : 파이썬의 for문과 비슷하나. 받아들이는 자료형이 Dictionary이다. 
<br> let obj = {a: 1, b: 2, c: 3};
<br> for (let v in obj) {
<br>     console.log(v);
<br> }
<br> 결과 : a b c
- key값을 반환하지, value값을 반환하지 않는다. 또한, 엔진에 따라 거꾸로 계산할 수 있어 잘 사용하지 않는다.

2. for .. of : 이게 파이썬의 for문과 비슷하다.
<br> for (let ch of "Hello") {
<br>    console.log(ch);
<br> }
<br> 결과 : H e l l o
- "Hello" 대신에 배열을 사용하는 것도 가능하다.

## 함수 선언.
- 기존에 함수를 선언할 때 function을 붙여야 했다면, 이제는 const를 사용하여 선언한다.
- 표기 방식에도 변화가 있다. 
- 디폴트 인자가 사용이 가능하다.
- ES5 :
<br> function add(x, y) {
<br>  var sum = x+y;  
<br>  console.log(sum);
<br> }

<br> var arr = [2, 3, 7, 8];
<br> arr.forEach(function(el) {
<br>  console.log(el * 2);
<br> });

- ES6 :
<br> const add = (x, y) => {
<br>  let sum = x + y;  
<br>  console.log(sum);
<br> }

<br> const arr = [2, 3, 7, 8];
<br> arr.forEach(v => {
<br>  console.log(v * 2);
<br> });

- ES6 함수 중 인자가 하나만 있거나 없을 때 :
<br> const greet = x => "Welcome " + x; // 인자가 하나만 있을 때.
<br> const x = () => alert("Hi"); // 인자가 없을 때.

## Object
