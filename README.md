## 자세한 것은 <a href="https://www.sololearn.com/Play/JavaScript">SoloLearn-JavaScript</a>, <a href="https://medium.com/ecmascript-2015">Medium</a>, <a href="https://developer.mozilla.org/ko/docs/Web/JavaScript">Mozilla-JavaScript</a> 참조 바랍니다.
## 의견 추가나 수정은 언제나 환영입니다!
<hr>

# HTML5 문법

=========================

##### <~> : 태그의 시작을 표시하는 기호.
##### </~> : 태그의 마지막을 표시하는 기호. 사용하지 않는 태그도 있음.
#####  밑에 나오는 요소들에 다 태그를 붙여야 함!

=========================

## &lt;!DOCTYPE html&gt;
### - 문서 형식 표시

## &lt;head&gt;, &lt;/head&gt;
### - 홈페이지에 필요한 문법들을 미리 로딩하거나 설명할 때 사용(탭 위에 마우스 가져다 놓으면 나오는 설명들을 여기에 설정함.)

### - 대표적으로 들어가는 요소들
1. &lt;meta charset = "utf-8"&gt; : meta 태그는 홈페이지의 설명을 담당함. 이 예제는 홈페이지의 인코딩 방식을 정의함.
2. &lt;title&gt; &lt;/title&gt; : 탭에 뜨는 페이지 이름을 설정함.
3. &lt;link&gt; &lt;/link&gt; : css 요소를 불러옴.
4. &lt;style&gt; &lt;/style&gt; : css 요소를 바로 선언함.
5. &lt;script language = "javascript" type ="text/javascript" (ES6 스크립트) /script&gt; : javascript 요소를 사용함.
6. &lt;noscript&gt; (문장) &lt;/noscript&gt; : 사용자가 스크립트 제한을 했을 때 화면에 나타내주는 태그.
7. &lt;base href="(도메인)" target="_blank&gt; : a 태그가 비었을 때 기본으로 사용하는 태그.

## &lt;body&gt;, &lt;/body&lt;
### - 홈페이지에 보여질 것들을 설정할 때 샤용.

### - 대표적으로 들어가는 요소들 (중요!)
1. &lt;div class="(설명)"&gt; (제목) &lt;/div&gt; : 컴퓨터의 폴더라고 생각하면 편함. 제목이 홈페이지에 보임.
2. ***&lt;h1&gt; &lt;/h1&gt;, ... , &lt;h6&gt; &lt;/h6&gt; : 글자의 크기를 표현. 숫자가 높을 수록 크기가 작음. README.md의 #과 동일함.
3. ***&lt;hr&gt; : 줄바꿈.
4. ***&lt;p&gt; &lt;/p&gt; : 문장을 표시함.
5. &lt;a href="(도메인)"&gt; (문장) &lt;/a&gt; : 하이퍼링크. p 태그 내부에 선언할 수 있음.
6. &lt;ul&gt; &lt;/ul&gt; : 점으로 분리해 문장을 설명함.
7. &lt;ol&gt; &lt;/ol&gt; : 번호대로 분리해 문장을 설명함.
8. &lt;li&gt; &lt;/li&gt; : ul 와  ol  태그 내부에 선언함. 보일 아이템을 선언한다.
9. &lt;br&gt; : '\n'과 동일한 태그.
10. &lt;iframe src="(도메인)" title="(설명)"&gt; &lt;/iframe&gt; : 조그만 창에 도메인을 불러오고, 설명하는 태그.

<hr>

# JavaScript (ES6Script)
- ES6의 중요한 부분으로 생각한 것만 다룹니다.

## 변수
1. var, let
- var은 전역변수, let은 C, C++의 for(int i = 1; i < n, i++)에서의 i (지역변수라 하나?).
2. const
- 변경 불가능한 변수를 선언할 떄 사용함. 그 외에는 let 과 같은 기능을 수행한다.

## 문자열
- 간편하게 사용할 수 있어 개인적으로 중요하다고 생각한다. 
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
<br> 결과 : a
<br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; b
<br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; c
- key값을 반환하지, value값을 반환하지 않는다. 또한, 엔진에 따라 거꾸로 계산할 수 있어 잘 사용하지 않는다.

2. for .. of : 이게 파이썬의 for문과 비슷하다.
<br> for (let ch of "Hello") {
<br>    console.log(ch);
<br> }
<br> 결과 : H
<br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; e
<br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; l
<br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; l
<br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; o
- "Hello" 대신에 배열을 사용하는 것도 가능하다.

## 함수 선언
1. 기존에 함수를 선언할 때 function을 붙여야 했다면, 이제는 const를 사용하여 선언한다.
2.  표기 방식에도 변화가 있다. 
3.  디폴트 인자가 사용이 가능하다.
- ES5 :
<br> function add(x, y) {
<br>  var sum = x+y;  
<br>  console.log(sum);
<br> }
<br> var arr = [2, 3, 7, 8];
<br> arr.forEach(function(el) {
<br>  console.log(el * 2);
<br> });
<br> 결과 : 4
<br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 6
<br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 14
<br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 16

- ES6 :
<br> const add = (x, y) => {
<br>  let sum = x + y;  
<br>  console.log(sum);
<br> }
<br> const arr = [2, 3, 7, 8];
<br> arr.forEach(v => {
<br>  console.log(v * 2);
<br> });
<br> 결과 : 4
<br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 6
<br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 14
<br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 16

- ES6 함수 중 인자가 하나만 있거나 없을 때 :
<br> const greet = x => "Welcome " + x; // 인자가 하나만 있을 때.
<br> const x = () => alert("Hi"); // 인자가 없을 때.

## Class
1. 클래스 생성방법
- class 바로 다음에 이름을 설정한다.
- constructor로 받을 인자를 설정한다.
<br> class Rectangle {
<br>  constructor(height, width) {
<br>    this.height = height;
<br>    this.width = width;
<br>  }
<br> }

2. 클래스 내부의 매소드 사용
- 매소드(method) : 객체(오브젝트, object) 내부의 함수.
- get : 객체 내의 변수에 접근할 때 사용하는 변수 설정자(?)라고 보면 편하다.
- static : get과 비슷하다. get은 (변수).(함수) 꼴로 선언하지만, static은 (클래스명).(함수)로 선언한다. <a href="https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Classes/static">Mozilla.</a>의 설명 참조.
<br>class Rectangle {
<br> constructor(height, width) {
<br>    this.height = height;
<br>    this.width = width;
<br>  }
<br>  get area() { 
<br>    return this.calcArea();
<br>  }
<br>  calcArea() {
<br>    return this.height * this.width;
<br>  }
<br>  ststic sentence() {
<br>    return 'static method has been called.';
<br>  }
<br> }
<br> const square = new Rectangle(5, 5);
<br> console.log(square.area);
<br> console.log(Rectangle.sentence());
<br> 결과 : 25 
<br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; "static method has been called."

3. 상속
- super : 부모의 클래스에서 변수를 사용할 때 사용한다.
- 자세한 설명은 <a href="https://medium.com/ecmascript-2015/es6-classes-and-inheritance-607804080906">Medium</a> 참조.
<br> class Vehicle {
<br>  constructor (name, type) {
<br>   this.name = name;
<br>    this.type = type;
<br>  }
<br>  getName () {
<br>    return this.name;
<br>  }
<br>  getType () {
<br>    return this.type;
<br>  }
<br> }
<br> class Car extends Vehicle {
<br>  constructor (name) {
<br>    super(name, 'car');
<br>  }
<br>  getName () {
<br>    return 'It is a car: ' + super.getName();
<br>  }
<br> }
<br> let car = new Car('Tesla');
<br> console.log(car.getName()); 
<br> console.log(car.getType());
<br> 결과 : It is a car: Tesla
<br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; car


## Promise
- 조금 까다롭다.
- 간단히 표현하면, 참과 거짓을 이용해 함수를 간단히 표현하는 것이다.
<br>function asyncFunc(work) {
<br>  return new Promise(function(resolve, reject) {
<br>    if (work === "")
<br>      reject(Error("Nothing"));
<br>    setTimeout(function() {
<br>      resolve(work);
<br>    }, 1000);
<br>  });
<br> }
<br> asyncFunc("Work 1") // Task 1
<br>.then(function(result) {
<br>  console.log(result);
<br>  return asyncFunc("Work 2"); // Task 2
<br> }, function(error) {
<br>   console.log(error);
<br> })
<br> .then(function(result) {
<br>  console.log(result);
<br> }, function(error) {
<br>  console.log(error);
<br> });
<br> console.log("End");
<br> 결과 : End 
<br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Work 1
<br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Work 2

## Module - 우린 React를 사용합니다!
- <a href="https://dojang.io/mod/page/view.php?id=2441">파이썬에서의 import</a>와 비슷하고, <a href="https://dojang.io/mod/page/view.php?id=802">C에서의 extern</a>과 비슷하다.
<br> // lib/math.js
<br> export let sum = (x, y) => { return x + y; }
<br> export let pi = 3.14;
<br> // app.js
<br> import * as math from "lib/math"
<br> console.log(`2p = + ${math.sum(math.pi, math.pi)}`)
<br> 결과 : 2p = 6.28
