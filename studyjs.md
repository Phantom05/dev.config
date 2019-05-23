js 예제해보기/ css 그라데이션 만들어보기.
window.onload= function(){
​	익명함수 = > 최초 한 번의 실행만을 필요로 하는 초기화 코드
지역변수 사용시 반드시 var과 같은거 사용 안그럼 전역변수됨
스코프 체이닝-> 내부함수는 자신을 둘러싼 외부 함수의 변수에 접근 가능하다.
내부함수는 일반적으로 자신이 정의된 부모 함수 내부에서만 호출 가능
()()사용하는 이유 -> 함수를 변수에 넣고 그변수를다시 ()하면 내부함수까지 실행됨
}
1.색갈 넣기, 콘솔, 얼랏, 프롬프트, 변수에 넣어서하기, 함수형인만큼 함수로하기.
버튼 클릭시 클로저를 이용한 도큐먼트에 붉은색으로 입력하기, 
함수로사용,변수선언,innerHTML 사용
replace,

2.typeof()사용해보기, 배열만들기, 배열의 길이확인하기 변수 문자열 합쳐서 렝스 출력, .slice()사용하기. 하나인자일경우 선택 이후모두 반환, 2개일경우 start,end로 됨end는 선택한게 잘리지않고 -1인덱스로하여금 짤림.그래서 원하는곳까지 자르려면 선택한인덱스+1로 계산하여 잘라주면 됨.

3.if문으로 조건걸어서 만들어보기,if문으로 데이터줘서 토글효과 만들어보기, 그리고 삼항식으로 그 토글효과 구현하기, 모듈러이용,inNaN사용해보기 toFixed 사용해보기, 오늘의 날짜 date로 구해보고 년도,달,요일,시간,분,초 구해보기, setInterval로 매순간 시간초 내는거 만들어보고 clearInterval하기 년 월 일 시간 다구하는것 변수에 넣어서 만들기 그리고 날짜에 0넣어서 만들기

4.while문 사용하여 10까지 출력, 함수 만들어서 매개변수 이용하여 함수에 값 반환
10에서 0까지출력, 3빼고 모두출력,for,while, do while

5.논리 연산자 사용하여 이프엘스문 만들어보기,toUpperCase,toLowerCase()이용하며 조건문 만들어보기. 변환하여 확인하고 보여줄 순 있으나 원래 문자열을 바꾸진 않음.

6.짝수, 홀수 출력 ,while,for,do while을 이용한 10까지 출력, 도중에 빠져나가기,
continue 이용하여 짝수빼고 모두 출력for,while, do while
countinue 이용하여 4부터 출력하기 10까지

7.번 - 9,7,5,3,1 출력, 구구단 출력, 구십구단 출력(입력 받았을때),split()사용,join()사용해보기

8.자스 버튼클릭시,1씩 값증가. 1씩 감소, 제이쿼리로도

9.스위치문 이용하여메뉴선택 만들기(프롬프트이용),if이용하여 입력 안했을때도 적용하기,while문 합쳐서만들기

10. !=이용하여 if문 만들어보기, 반복문과 continue,break사용
11. 함수 만들어 return 값으로 저장하기, 매개변수 이용하여 함수를 만들어 콘솔로그 찍기. %, / 뜻 알고 if문 만들어보기.
12. 단항 연산자, 변수에 a 넣고 -a 하면 -됨.

13.다항연산자 ++a, a++사용해보고 += 사용하여 반복문 만들어보기

14.Math.pow, Math sqrt, Math.random,Math.ceil Math.floor.,Math.round, Math.abs,Math.max,Math.min,Math.PI 프롬프트에 들어간것은 숫자가 들어가도 type이 string으로됨. 때문에 .문자열을 숫자열로 바꿔야해줘야함 그 메소드가 parseInt와 parseFloat임

15.이스케이프 \' \\이용 , object = 객체같은말...ㅋ이걸이제.ㅋ.ㅋ

16.객체,배열 이름에 접근하기 .이용 []이용, 빈오브젝트 만들고 추가해보기, 객체만들고 콘솔로 키값만 출력해보기 for in문, for문
언디파인 = 속성이 정의되어있지 않음을 표현, null 개발자가 임의로 비어있다고 선언.null 은 비어있는 객체라고 정의한거임 typeof찍어보면 언디파인이아니라 object로 나옴

17.return을 하면 return 옆의 값을 해당 함수에 넣어주는 것임.
조건을 이용할떄 논리연산자 && 에서 true true면 나머지는 모두 false ||에서는 false false 빼고 다 true 이거 이용해서 조건문 만들어보기.

18.연산자 순위 이용하여 계산해보기 !  */%+-, ><<=>===!=  && || 순

19.concat() 이용하여 문자 붙이기. 문자열 숫자열 더하고 typeof찍어보기 그리고 그것의 length를 구해 다른 변수에 넣기. 

20.charAt 이용하여 값 특정 문자에 접근하기., 대괄호로도 접근하기
length이용하여 마지만 문자값 구하기. .substring()와 substr()비교하여 특징 알아두기. 또한 숫자 1개만 인자로 넣었을때 확인. -값도 확인. .indexOf()사용하여 반환하기, lastIndexOf()사용해보기 같은 글이 2개잇을때 앞쪽에 있는 가장 첫번쨰 문자열 인덱스반환 index 뒤쪽의 앞쪽문자열 반환 lastIndexOf
indexOf = 맞으면 문자열의 인덱스를 반환 없으면 -1반환
있으면 첫번쨰 문자를 인덱스 번호로 반환함.

21. 배열 만들어보기, 객체, 다양한 자료형 넣기, pop push, shift, unshift 사용해보기. .sort() 사용하기. concat이용하여 배열합치기.
    위의 메소드 이용해서 문장 만들어보기.

22.그냥 문자에 split()사용해보기 ","힌트, 두개의 조건을 넣어 논리연산자이용 만들어보기, 4의 배수의 if문 작성+=, %사용

23.for문을 이용해서 배열 cost의 값을 모두 더해 total_cost 변수에 저장하세요. 
var cost = [ 85, 42, 37, 10, 22, 8, 15 ];
var total_cost = 0;

24.객체를 만들고 Object.keys()로 키값 확인해보기.
for in 문을 이용해 객체의 속성에 접근해보기. 포문, 포인문 써보기. 배열을 for in문으로도 출력해보기, in연산자로 미리 확인해보기 속성이 있는지.

25.for in 문을 이용해서 obj의 속성중, number 타입의 값을 모두 더해서 sum에 저장하도록 코드를 수정하세요.
_____ 부분을 수정하면 됩니다.
var obj = {
​	name: "object",
​	age: 10,
​	weight: 5
}
var sum = 0;
for ( ____ in ____ ){
​    if( typeof( ____ ) == "number" ){
​        sum = sum + ____;
​    }
}

26.함수 내부의 에서 함수 내부만 가능함 , shadowing 문제 풀어보기. 
같은 이름의 변수를 함수 내부에서 그리고 외부에서 사용할때 함수를 호출해서 같은 이름의 변수를 함수내부에서 ++해준다고 해도 밖에서 console.log할때 전역변수로 사용된 변수의 값을 콘솔창에 띄움.

다음 코드는 구구단을 2단부터 9단까지 출력하는 코드입니다. 하지만 이대로 실행하면 정상적으로 구구단을 출력하지 않습니다.
아래의 코드에 shadowing 효과를 추가해 구구단이 잘 출력되도록 하세요.

function printTimesTable(a){
​	for( i = 1 ; i <= 9 ; i++ ){
​		console.log( a + " * " + i + " = " + a*i );
​	}
}

for( var i = 2 ; i <= 9 ; i++ ){
​	printTimesTable(i);
}



27.객체 안에들어가는 함수는 메소드 , 객체 안에 함수 넣을떄 
method:함수이름만()말고 쓰면 들어감. o.함수명(); 이렇게 함수 호출도 가능함.
매게변수를 이용하여 this.객체 접근하여 키값 변경해보기// 함수안에서는 전역으로 빠짐. 'use strict' 사용해보기

객체안의 메소드로 사용될떄 this는 객체 자기자신이다 this === 메소드가 포함된 객체자신 찍어보기,

하지만 객체안의 메소드 안의 함수는 this를 찎으면 메소드를 포함한 객체일때 false를 반환한다. 즉 함수안의 this이기 때문에 window를 기준으로 삼는다.

.call() - > 객체의 메소드 안의 함수에서 this가 전역객체를 가르킬때 call을 메소드안의 함수말고 메소드안에서 call(this)를 붙혀주면 메소드와 동일하게 메소드가 포함된 객체가 this로 잡히기 때문에 메소드 안의 함수에서 this를 메소드를 포함한 객체로 사용할 수 있따.// 메소드사용할때만 사용하기 때문에 객체.메소드.call()을 사용해줘야한다. 대신 원래의 함수에는 반드시 this가 있어야겠지 그래야 call로 바뀐놈에서 무언갈 가져올테니까.
또한, call에서 1개만 호출하지 않고 콤마(,)로 구분해서 하나 더 넣어주면 매게변수로도 사용 할 수 있다. 대신 원래 함수에서 매개변수를 (y)해주고 그것을 y로 사용한 상태여야 야겠지 아래 예제를 보자
즉 .call이든 apply든 .메소드(함수명,인자)이렇게 해야함.

calll 간단예제

> var a = { x: 1 };
> var b = function () { console.log(this.x); };
> b.call(a);
> // 1
> call은 arguments를 콤마로 구분, apply는 배열로 받는다.

call 심화예제

```js
var numbers = {
​            numberA: 5,
​            numberB: 10,
​            sum: function() {
​                console.log(this === numbers); // => true
​                function calculate() {
​                    console.log(this === numbers); // => true
​                    return this.numberA + this.numberB;
​                }
​                // 문맥을 수정하기 위해 .call() 메소드를 적용
​                return calculate.call(this);
​            }
​        };
```

> var a = { x: 1 };
> var b = function (y) { console.log(this.x + y); };
> b.call(a, 1);
> // 2
> b.apply(a, [1]);
> // 2

apply는 그냥 메소드에서 1개의 인자로 만 사용하면 call과 동일하다 하지만 매게변수를 받을때 apply는 배열로 받게된다.
apply 간단예제

```js
function sum(aa,bb){
​            return aa+bb
​        }
```

sum.apply(null,[2,4]) - > 이게 기본 구조임 배열로 들어가는것
sum(2,4)이렇게 호출할 수도 있지만 저렇게 호출 할 수도 있음.
또한. 기본 구조는.

```js
o1 = {val1:1, val2:2, val3:3}

function sum(){
​    var _sum = 0;
​    for(name in this){
​        _sum += this[name];
​    }
​    return _sum;
}
```

이렇게 되있을떄  이 함수를 ol의 객체로 넣어주고 싶을때
 ol ={name:'jun',age:20,sum:sum(aa,bb)}.이렇게 하고
ol.sum()이런식으로 호출을 해야하지만 그렇게 되면 객체로 자기자신의 키값까지 포함시켜서 if(typeof this[name] !== 'function')이라는 조건문을 넣어줘야는데 이렇게 불편함을 방지하기 위해 만들어져 나온 객체메소드가 바로 apply이다.

sum.apply(o1); 이렇게 사용하게되면 o1안의 속성인거 처럼 사용하여 간편하게 6의 답을 얻을 수 있다.//★

또한 예약어 class를 생성한 new를 이용했을때도 this는 역시 객체 자기 자신임을 알수있따.

또한 class예약어 - >미리만들어논 함수 에서 함수를 키:메소드로 바로 넣지않고 변수안에 넣는 경우도 있다. 
변수 = function(){
}이런식으로 될때 함수안의 this는 window를 가르키게 된다.
var earth - new Planet('Earth');
// 메소드 실행. 여기서의 this는 earth

함수를 변수에 저장하면 변수를 호출할때 함수처럼 호출해줘야함.변수() 이렇게

28.매개변수 array의 평균값을 return하도록 함수를 만들어 보세요.
array는 정수만을 저장하는 배열입니다

function average(array){
  //함수를 완성하세요
}

console.log(average([1,2,3]));

어떠한 비어있는 변수에 +=에서 쌓고싶다면 문자를 쌓을땐 이렇게 '';비어있게  숫자를 쌓을떈 null이나 0으로 초기화를 해주고 사용해야함 
var sumA += x; 는 var sumA = sumA + x이렇게 되기 때문에 틀린거임 sumA = sumA + x 로 만들어줘야함.



29. 반쪽 삼각형, 반쪽 역삼각형 찍기.

FOR문에서 컨티뉴하면 먼저 증가하고 조건식을 검사함.
for문, while문에서는 i++, ++i의 차이가 없음

```js
function sumFrom1ToN(n){
​    var count = 1;
​    var sum=0;
​    while( count <= n){
​        sum = sum +count;
​        count++;
​    }
​    return sum;
}
```

이거이해하기

30.arguments = 사용자가 인자로 넣은것을 배열로 넣음
함수의 이름.length하게되면 매개변수의 숫자를 알려줌
arguments.lenghth 함수의 매게변수로 들어간 숫자.

이중 배열을 만들어 안쪽에 들어간 배열의 인덱스로 문제와 답 확인하여 빈 배열에 쌓아보기 2개이상 [,]콤마 뒤가 정답이여야함.그리고 그걸 메세지로 스코어를 콘솔로 띄우기. 답보지말고

let score = 0;
​        let question=[
​            ['준영이의 팔의 개수는?',2],
​            ['준영이의 다리의 개수는?',2],
​            ['준영이의 머리의 개수는?',2]
​        ]
​        for(let i =0;i<question.length;i++){
​            askQuestion(question[i]);
​        }
​        function askQuestion(question){
​            let answer = prompt(question[0])
​            if(answer === question[1]){
​                console.log('축하합니다. 정답입니다.');
​                score++
​            }else{
​                console.log('틀렸습니다.')
​            }
​        }
​        let message = '최종 점수 :'+score;
​        message += ' / 전체 :'+question.length;
​        console.log(message);



31.

클로저 이해하기
function makeCounterFunction(initVal){
​    var count = initVal;
​    function Increase(){
​        count++;
​        console.log(count);
​    }
​    return Increase;
}

var counter1 = makeCounterFunction(0);
var counter2 = makeCounterFunction(10);
return 한상태로 값을 변수에 저장하니 값이 나눠짐.

삼항식 써보기 ? a:b
condition ? expr1 : expr2 
파라미터
condition (or conditions)
true 혹은 false로 평가되는 표현식
expr1, expr2
모든 형식의 값을 지닌 표현식
예제
var age = 29;
var canDrinkAlcohol = (age > 19) ? "True, over 19" : "False, under 19";
console.log(canDrinkAlcohol); // "True, over 19"

--
Event 종류
form, window, mouse, key

1선택한엘리먼트 앞 뒤 엘리먼트 만들어보기, 자식 앞 뒤 엘리먼트 만들어보기
createElement, createTextNode
.nextElementSibling
.previousElementSibling 사용해보기.
.children[]
.parentNod
for문 이용하여 

-생성-
var $div = $('<div>Hello</div>');
var div = document.createElement('div');
var text = document.createTextNode('Hello');
div.appendChild(text);

2. 변수에 저장하는 이유 = 편의
   document.getElementById()
     document.getElementTagName()
     document.getElementsByname()
     innerText, innerHTML
     .style로 변경 
     .getAttribute()
     .setAttribute(,)
3. input태그에 적용되는 .value속성 이용 하여 값 가져와보고 수정해보기. querySelector 사용하기 여러개의 클래스를 반환할때는 첫번쨰껏만 반환됨. querySelectorAll 해도 모두 가져올 뿐이지 똑같이 배열형식으로 저장됨.

4.createElement, appendChild이용하서 추가해보기
도큐먼트 클래스네임이나 복스로 가져오면 배열 형식으로 저장됨.insertBefore(인자1, 인자2) 사용해서 원하는곳엘리먼트 앞쪽으로 넣어보기. cloneNode()사용하기., removeChild이용하 삭제해보기.

5.setInterval, setTimeout 이용해보기 clearInterval, arguments 사용해보기

6.인클라인 onchange, keydown, 프로퍼티 방식으로 만들어서 효과줘보기, addEventListener 사용해보고 removeEventListener사용해보기

7.AJAX통신연습. new 객체 생성 후 open, send하면 요청 끗
.response 찍어보기 통신 요청 후
.readyState 찍어보기 - 단계별로
.onreadystatechange만들기. // readystate가 변경될 때마다 안에 등록된 함수가 호출 되는 것임.
함수 안에  console.log(this.readyState) 찍어보기.
.status찍어보기, 응답 상태를 나타냄
반응은 하지않지만. if문 만들어서 조건 &&로 걸은 후 
안에 .responseText 사용하기

8.JSON. = 자바스크립트 객체를 문자열로 표현하는 방법.제이슨은 메소드나 언디파인은 변환되지 않고 요소들만 문자열로 바꿈.  숫자형, 문자형, 배열, 객체 만든후 
그리고 그걸 변수에 넣어보기

확장자명은 json으로 보내고
2개이상 객체 만들어서 제이슨 파일로 전송해보기.
넘길 json 객체가 2개이상일 경우 [,]로 2개이상의 객체를 넣어준다.
그리고 객체의 키와 벨류값 앞에 역슬레쉬를 해줘야 파일이 전송될때 엔터키가되서감
=전송=
JSON.parse() 사용하여 해동시키기 , 변수에 넣고 그변수를 사용 -> 자스의 인자로 만들어줌.// parse하지않으면 json파일을 사용할수 없음 고로 json파일로 모두 사용하지만 각각언어에서 parse해서 사용하는것임.

또한 양끝에 ' '로 문자로 전송했을때, 그걸 파스하면 객체로 바뀜
JSON.stringify() 사용해보기 //시리얼라이즈드라고함.
이걸 제이슨 포맷으로 변형한 텍스트를 만드는것임.

9.팝업창 띄우기. window.open('주소',팝업창이름,'넓이,높이,레프트,탑'), 온클릭, 온로드,익명함수 만들어보기.

10.예외처리 해보기 try,catch,finally,throw, classList toggle이용해보기. if문으로 setAttribute이용하여 클래스 확인 후 토글 만들어보기 -> 함수안에서 사용함

인라인으로 onload=함수명 을할떄 함수명()하면 바로 실행하지만 ()을 없애면 모두 로드되고 실행함.

11.함수따로뺴서 객체에 이름만 넣은 메소드 만들어보기.

--

------

제이쿼리. 자스랑 섞어쓰려면 인덱스를 설정해줘야함.
삼항식 만들어보기 2개이상 2개의조건
생성 - 추가 - 제거 해보기
append, appendTo,prepend, prependTo 사용
after, insertAfter, before,Afterbefore 사용
클래스만들어놓고 넣을떄 클래스명 정해서 넣기
To사용할떈 앞에있는건 변수에 넣어야함, 또한 하나의 변수의 엘리먼트는 하나씩만 넣고 뺴고 할 수 있음.
ready()대신 $(function(){
}이렇게 쓸수도 있음.

clone사용 remove,detach,empty사용

1.body에 h1 추가, 속성 선택자 이용해보기., 속성^= , $=. *=사용해보기, 필터 사용해보기 even,odd,not ,has,contains,hidden,visible,

2.show(),hide(),text(),fadeIn(),fadeOut(),fadeTo(,)사용하기 //체이닝이라고함, 또한 $('#banner').innerHTML 이러면 제이쿼리 객체에서 뒤에껄 읽을수 없음 생각하자 쩜은 객체로 이동이니까 저 객체에서 이동했을때 js객체인 innerHTML이 있겠니..

제이쿼리는 루프기능을 모두 포함하기 떄문에, 선택자를 선택후 for을 쓸필요가 없음 느려지는 원인일지도.

slideDown(),slideUp(),slideToggle()사용하기

3.html()->값을 입력안하면 선택자의 값을 반환 입력하면 내용 바뀜 innerHTML과 같은기능 text()는 텍스트만/.offset()사용//, 셋인터벌,오프셋 사용해서 왼쪽으로 가다가 초기화되는 애니메이션 만들어보기, event.pageX,event.pageY사용, click이벤트 이용하여.절대좌표 아님. 브라우저 기준. 

4. mousemove()이용하여 offset으로 움직일떄 따라다니는기능 만들기. 데이터값을 만들어 셋인터벌,오프셋을 사용하여 오우왼위로 움직이는거 만들기

5.addClass 사용,removeClass,toggleClass사용, css사용, 토글클래스시 토글되는 클래스가 아래있어야함 케스케이팅, 제이쿼리는 자식요소뿐만아니라 형제요소도 바꿀수잇음. 형제의 자식도 됨.
제이쿼리에서 이벤트사용시 this는 이벤트가 발생한 객체를 가르킴
css는 ('','')이런식 애니메이트는 ({'':'',})이런식
css여러개 줄시 ({'':'','':''})이렇게 주면됨

6.attr사용하여 설정,제거
attr('src')하면 태그명반환, ('','')하면 속성면경,, rem,oveAttr()하면 제거
.each() 사용해보기- 존재하는만큼 실행됨, 또한 함수안에매게변수를 넣을시 인덱스로 적용됨. 0부터 출력 찾은만큼

7.clone()써보기 한번만 복제해도 계속 사용가능. 
pq라는 클래스 span태그 추가
각각의 span태그 복제
복제한 span태그의 클래스명 제거 pullquote라는 클래스명 추가;
html문서에 삽입.

모든 이벤트는 바로 함수로 넣지말고 함수를 미리 만들어 놓은 후 함수 명을쓰기. 그리고 이벤트에 함수를 전달할때는 ()괄호를 생략하고 함수명만 써야함.

8.마우스 이벤트
테이블 만들어서 click, dblclick,mouseover,mouseout,mousedown,mouseup,mousemove,hover써보기
hover는 온이벤트가 안먹음.toggle도 온이 안먹음
add클래스 remove클래스로 해보기, toggle이벤트 써보기
-클릭했을때 x, y좌표 콘솔에 찍기
$(document).click(function(evt){
​                let xpos = evt.pageX;
​                let ypos = evt.pageY;
​                console.log('x :',xpos,'y :',ypos)
​            })
//특정행위를 했을때 evt로 저장됨 //pageX,Y screenX,Y사용

9.document.window 이벤트
load,resize,scroll,unload사용해보기

10.form이벤트
submit, reset,change,focus,blur 사용해보기

11.키보드이벤트
keypress,keydown,keyup 사용보기

12.기본 이벤트 멈추기
여기서 e는 함수구현후 매게변수로 이동될것을 연결해준다.
e.preventDefault();
이거대신 아래 return false; 사용해줘도됨.
그리고 이벤트를 제거할떄는 $('').unbind('이벤트명')하면됨
온 바인딩 이용하여 on('click',객체,함수)하여 객체내용을 함수에 붙혀 얼랏 띄어보기

13.토글로 질문 클릭시 답변 나왔다 들어가게 하는데 3개이상 만들어보기 next()이용

14.animate
.animate({margin:'50px',opacity:''},밀리세컨드)이런식으로 사용
저안에 +=사용하면 클릭할때마다 중첩됨 '+=50px' 이런식

15.네모모양으로
왔다갔다 하기 offset({left:x,top:y})이용하기, 마우스 따라다님 만들어보기

-클릭 함수에 특정 이벤트가 있는 놈을 셀렉터로 언바인트 해놔서 클릭시 이벤트 종료하게하는 기능 만들어보기.

함수말고 그냥 전역에다 'use strict';를 사용하면 이 라인 이후로 모두 적용된다. ie10 이상에서 사용됨.생성자 인스턴스에 속성을 추가하면 생성자에 추가됨.

스코프체인, 지역,전역함수, 스코프는 함수를 호출할 때가 아니라 선언할 때 생깁니다. 정적스코프라 불림.// 선언할때 0번으로 전역객체에 변수가 있으면 그 변수가 들어가고 다른 함수에서 호출됬을때 그 함수내에 또 동일한 이름의 지역변수가 있으면 그변수가 두번째 1번으로 들어가게됨 때문에 0번이 먼저실행되서 처음 전역에 함수가 선언될때 전역 변수로 된게 실행되는것임.

16.canvas만들어보기 getContext('2d');,fillRect, fillStyle='';3개이상사용
strokeRect,strokeStyle,lineWidth
strokeStyle,lineWidth,beginPath, moveTo,lineTo,stroke 사용//beginPath = 시작을 알림 moveTo좌표로찍고 lineTo좌표찍으면 stroke를 이용하여 선이 그어짐
beginPath로 시작을 알리고 moveto로 시작점을 찍은후 lineTo로 5개정도 찍은다음 fill, fillStyle을 적용해서 집 만들어보기. 최대 5개까지됨

17.내부함수 사용시 첫번쨰 메소드에다가 var that = this 해놓으면 내부함수에서 계쏙 메소드를 컨택할 수 있음.

Polifill shim 복습
<-- [if It IE 9]

<script src="경로/html5shiv.js"></script>

<![endif]-->
자스 함수는 항상 리턴함.
리턴을 써주지 않을경우 언디파인을 리턴함.
생성자한수에서는 this로 바인딩된 새로운 객체를 리턴하기 때문에 따로 리턴을 써주지 않아도 된다.

생성자함수로호출해서 새로운 객체를 생성해도 리턴값이 명시적으로 배열이나 객체로 정해져 있으면 리턴값으로 리턴됨.//리턴으로 넘긴값이 불린숫자문자열일경우는 그냥 this로 바인딩 된 객체가 리턴됨.

/* 마스터북 */
1.분할대입 해보기., ...other 사용해보기, 변수 교환해보기, 배열,객체.
== 을사용할때 참조형일경우에는 내용이 같아도 false가 출력된다 예를들면 배열을 두개 비교하는데 배열 명이 다르다 하면 배열의 경우 일정 메모리공간에서 참고하기 때문에 false가 나오고 숫자2개를 비교하는건 기본형으로 값자체를 비교하므로 true가 나오게 된다.
/**/

------

퍼블 페이지 한 섹션식 만들기
mdn 한글사이트 js
https://www.w3schools.com/xml/xml_http.asp
http://book.naver.com/bookdb/book_detail.nhn?bid=12199050
http://musu.me/88
https://opentutorials.org/module/1246/8173
https://opentutorials.org/course/1375/10037
html obfuscator
http://cssmenumaker.com/

주말마다 드롭다운 모두 따라 만들어보기
★css버전, jquery버전, javascript버전★

http://bqworks.com/slider-pro/#example1
http://kenwheeler.github.io/slick/
슬라이드
includ_once이용. -php
?<?=md5(microtime())?>
CSS Obfuscation
http://www.csswinner.com/

ajax에서
토글 효과를 만들떄 기본 변수로 ='true'로 하나 만들고
클릭할때 if문에 true로 실행될떄 만든 변수를 'falss'로 바꿔서 클릭할때 false로 바꾸고 또 다시클릭할떈 false상태에서 실행되는 if문을 만든 다음 그안에다가는 true로 변경하는 기존 변수를 넣는다. 

var userAgent = navigator.userAgent;
  alert(userAgent)
사용하는 기기 모바일인지 확인 가능함.

src만들어서 속성 조절해보기
sin cos 공부해보기

어펜드차일드는 node타입만 가능, 텍스트 노드안댐, 엘리먼트형식으로만
append는 다됨.

var students =[
​      {이름:'이준영',국어:98,수학:67,영어:97,과학:99},
​      { 이름:'선뚝백',국어:46,수학:10,영어:11,과학:07},
​      {이름:'똑똑이',국어:99,수학:98,영어:100,과학:95},
​      {이름:'똑똑이',국어:97,수학:86,영어:92,과학:89},
​      {이름:'모질이',국어:12,수학:09,영어:17,과학:50}
​    ]

```js
let success={'통과한 학생':[],"통과하지 못한 학생":[]}

let filterB = students.forEach((x)=>{
  return (((x.국어+x.수학+x.영어+x.과학)/students.length) > 50)?success['통과한 학생'].push(x.이름) :success['통과하지 못한 학생'].push(x.이름)
})
console.log('통과한 학생',success['통과한 학생'],'\n통과하지 못한 학생',success['통과하지 못한 학생']);
```

Math.random()*10-Math.random()*10

\cX

const abcd =(arg)=>Math.min(…arg)
console.log(abcd([5,-50,5,10]))

var m = new Map([[1, 2], [2, 4], [4, 8]]);
Array.from(m);   
var arr = Array.from([1,2,3],x=>x*10)
Array.from('Yaho')
Array.from({length:5})

기기확인해서 css 바꿔보기
클릭시 제이슨으로 내용 바꿔보기

 let arr =[
​      {
​        abc1:[
​        {name:'hello'},{age:50}
​      ]
​      },
​      {
​        abc2:[
​          {name:'world'},{age:100}
​        ]
​      }
​    ]

```
function func(n){
  return arr[n-1]['abc'+n][n-1].name;
}
console.log(func(1));
```

이렇게 타고드가도되고 기본적으로 0 1 2 3 인덱스가 있기때문에 이름은 abc로 통일해줘도됨.

span blind태그 접근성

return x.replace(/\d/g, d => d < 5 ? 0 : 1);

셀렉 타고가기
//캡쳐링 막기
e.stopPropagation()

try catch finally 부분 파보기

switch(true) {
case (true, 'abc'):
console.log('Hello')
  break;
case true:
case 'abc':
case false:
  alert('hi');
}
//이터레이터 
​    const book=[
​      'Hello1',
​      'Hello2',
​      'Hello3',
​      'Hello4',
​      'Hello5',
​      'Hello6',
​    ]
​    let it = book.values();
​    let current = it.next();
​    while(!(current.done)){
​      console.log(current.value);
​      current = it.next()
​    }
//이터레이터 독립성
​    const it1 = book.values();
​    let it1cureent=it1.next();
​    const it2 = book.values();

```
console.log('it2',it2.next())
while(!it1cureent.done){
  console.log('it1cureent',it1cureent.value);
  
  it1cureent = it1.next();
}
console.log('it2',it2.next())
console.log('it2',it2.next().done)
```

//배열 넣을때
​    let AAAB = [];

```
function add2(message) {
  return AAAB.push({message})
}
add2('Hello')
console.log(AAAB)
```

//피보니치 수열
​    function fibosu1(){
​      let a=0, b=1,c=0;
​      let res=[]
​      for(;;){
​        res.push(b)
​        c=a+b
​        a=b;
​        b=c;
​        if(c>100) break
​      }
​      return res
​    }
​    console.log(fibosu1());

// 맵활용
function digitize(n){
  return (n + '').split('').map(Number).reverse();
}

//피보니치수열
​    function fibosu2(tar){
​      const arr =[1];
​      const cur = arr.values();
​      let ta =cur.next();
​      let res=0;
​      while(true){
​        arr.push(res);
​        res+=ta.value;
​        ta = cur.next();
​        if(arr.length>=20) break;
​      }
​     return arr.slice(1)
​    }
​    console.log(fibosu2())
function disemvowel(str) {
  var vowels = ['a', 'e', 'i', 'o', 'u'];

  return str.split('').filter(function(el) {
​    return vowels.indexOf(el.toLowerCase()) == -1;
  }).join('');
}

Array from

Math.max.apply(0,[1,2])

```js
 let str = "ya ho ain't Hello!";
 String.prototype.toJadenCase = function () {
   return this.split(' ').map(x=>x.replace(x[0],x[0].toUpperCase())).join(' ')
```

   

```js
};
​    let str = "ya ho ain't Hello!";
​     String.prototype.toJadenCase = function () {
​       return this.split(' ').map(x=>x.charAt(0).toUpperCase()+x.slice(1)).join(' ')
​     };
​    let str = "ya ho ain't Hello!";
​    String.prototype.toJadenCase = function () {
​      return this.replace(/(^|\s)[a-z]/g,function(s){return s.toUpperCase()})
​    };
​    console.log(str.toJadenCase())

// function solution(number) {
// 	for (acc = 0; --number > 2;) {
// 		acc = !(number % 3) || !(number % 5) ? acc + number : acc;
// 	}
// 	return acc;
// }

// function solution(number) {
// let s = 0;
// for (let i = 0; i < n; i++) s += i % 3 ? i % 5 ? 0 : i : i;
// return s;
// 	}

  function validatePIN3 (p) {
​      return p.length==4 ||p.length ==6 && parseInt(p) ==p
​    }
​    console.log(validatePIN3('54g5f4'))
// 두번째 조건 지렸다..
```





```js
var setCookie = function (name, value, exp) {
  var date = new Date();
  date.setTime(date.getTime() + exp * 24 * 60 * 60 * 1000);
  document.cookie = name + '=' + value + ';expires' + date.toUTCString() + ';path=/';
};

setCookie('name', 'jun', 7)
console.log(document.cookie)

function getCookie(cookie_name) {
  var x, y;
  var val = document.cookie.split(';');

  for (var i = 0; i < val.length; i++) {
    x = val[i].substr(0, val[i].indexOf('='));
    y = val[i].substr(val[i].indexOf('=') + 1);
    x = x.replace(/^\s+|\s+$/g, ''); // 앞과 뒤의 공백 제거하기
    if (x == cookie_name) {
      return unescape(y); // unescape로 디코딩 후 값 리턴
    }
  }
}

getCookie()

localStorage.test = '123';
localStorage.setItem('test', '124');

localStorage.getItem('test');
localStorage.removeItem('test');
// localStorage 객체에서 원하는 값을 지우는 방법

localStorage.clear();
// 한번에 저장된 모든 값을 삭제하는 방법
localStorage.n1 = ['dd', 'ff']
localStorage.getItem('n1');

sessionStorage.setItem('domain', 'webisifree.com')
// domain이란 키(key) 값을 사용하여 해당 텍스트를 저장함

sessionStorage.getItem('domain')
// 키에 저장된 값을 반환. 여기서는 webifree.com이 출력됨

sessionStorage.removeItem('domain');
//domain 키와 데이터 모두 삭제

sessionStorage.clear();
// 저장된 모든 값 삭제

//인터넷 익스플로러 IE(Internet Explorer)는 10MB의 공간을 사용할 수 있고, 그 외 브라우저는 대부분 5MB의 공간을 사용할 수 있다. 사실 로컬 또는 세션스토리지 모두 사용되는 부분이 한정적이고 대부분 텍스트 공간을 차지하므로 용량이 부족하다던가의 이슈는 대부분은 없을 것이다.

//글 작성 중간 중간에 잃어버리지 않기 위한 임시 저장용도
// 장바구니나 좋아하는 콘텐츠 등 수시로 변경되는 경우
// 방문자의 이동 경로를 저장하였다가 이동할 경우
// 그 외 서버에 반드시 저장할 필요가 없는 경우

document.cookie = "test=abcde";

function setCookie(cookie_name, value, days) {
  var exdate = new Date();
  exdate.setDate(exdate.getDate() + days);
  // 설정 일수만큼 현재시간에 만료값으로 지정

  var cookie_value = escape(value) + ((days == null) ? '' : ';expires=' + exdate.toUTCString());
  document.cookie = cookie_name + '=' + cookie_value;
}

setCookie('myHobby', 'game', '3');
```

네임스페이스.

순서도 만들기

제로초 4-1
Math.random()은 랜덤할떄 사용하면 안됨.. 랜덤 라이브러리를 사용해야함 ㅋㅋㅋㅋㅋ



```js
var prop = 2;
var obj = { prop };
console.log(
  obj
)
var obj ={
  aaa:function(v){
    this.name = v
    console.log('hello')
  }
}
var aaa = new obj.aaa('jackson');
console.log(aaa)
var array1 = ['a','b','c','d','f'];
console.log(
  array1.copyWithin(3,1,2)
)
var array2 = [0,1,2,3,4,5];
console.log(
  array2.fill(9,1,3)
)

function compaireFunc(key){
  return function(a,b){
    return a[key] - b[key]
  }
}
var persons = [{name:"b",age:5},{name:"a",age:1},{name:"Tom",age:17},{name:"Huck",age:18},{name:"Becky",age:16}];
console.log(persons.sort(compaireFunc("age")));

 var a = [1,2,3,4,5];
 var sum = 0;
 a.forEach((v,i,a)=>{
   a[i] = v*v
 });
 console.log(a)




let testObj = ['Tom','Huck','Becky','Jack'];

  testObj.reduce((x,y)=>{
    x[y] = y.length
    return x
  },{})
//{Tom: 3, Huck: 4, Becky: 5, Jack: 4}



function f4(f1, f2, f3) {
  return f3(f1() + f2())
}
console.log(
  f4(
    function () {
      return 2;
    },
    function () {
      return 1;
    },
    function (a) {
      return a * a
    }
  )
);



// 2._filter
function _filter(users, predi){
  //필터는 응용형 함수, 원하는 시점에 조절할 수 있는 함수
  var new_list = [];
  for(var i = 0; i< users.length;i++){

    if(predi(users[i])){
      new_list.push(users[i]);
    }

  }
  return new_list;
  //콘솔로 소통하지 않고 리턴으로 소통하는게 좋다.
}
console.log(
  _filter(users, function(user){ return user.age >= 30;})
)
console.log(
  _filter(users, function(user){ return user.age < 30;})
)
console.log(
  _filter([1,2,3,4], function(num){return num%2}),
  _filter([1,2,3,4], function(num){return !(num%2)})
);

console.log('map')
// 3. map
//다형성이 높고 데이터를 함수에서 전혀 찾아볼 수 없게됨. 완전히 분리가됨
function _map(list,mapper) {
  var new_list = [];
  for (var i = 0; i < list.length; i++) {
    new_list.push(mapper(list[i]))
  }
  return new_list
}

var over_30 = _filter(users,function(user){return user.age >= 30});
console.log(over_30);

var names = _map(over_30,function(user){
  return user.name
});
console.log(names);

var under_30 = _filter(users,function(user){return user.age < 30});
var ages = _map(under_30,function(user){
  return user.age
})
console.log(ages);



console.log(
  _map([1,2,3],function(num){return num*2})
);

console.log(
  [1,2,3].map(function(val){ return val* val})
);
console.log(
  [1,2,3].filter(function(val){return val % 2})
);
// 기존의 map 과 filter는 메서드임. 순수함수가 아님.
// 또한 객체 지향 프로그래밍임.

//객체지향은 반드시 객체가 생겨야 메서드를 사용 가능하기 때문에, 평가 시점이 중요하다
try{
  console.log(
    document.querySelectorAll('*').map(function(node){
      return node.nodeName;
    })
  );
}catch(e){
  console.log(e)
}

// 반면 함수형 코드의 경우 함수가 이미 존재하기 때문에 평가시점이 훨씬 유연하게 된다.
console.log(
  _map(document.querySelectorAll('body'),function(node){ return node.nodeName})
);
// 다형성 면에서 좋다.


// 3. 내부 다형성
// 1. predi, iter, mapper
_map([1,2,3,4],function(v){ //두번째 인자는 보조함수, 내부함수의 다형성이 중요, 내부 다형성.
  return v+20
})
// 보통 두번째 인자로 함수가 들어가면 콜백함수라고 부르는 경우가 많은데./
// 함수의 역할의 이름을 따로 불러중요 하는것이 중요하다. 맵퍼이든지 이터이든지 프리디이든지.


// 커링 -> 원하는 인자의 조건이 채워졌을때 본체를 실행

function _curry(fn){
  return function(a){
    return function(b){
      return fn(a,b)
    }
  }
}

var add = _curry(function(a ,b ){
  return a+b;
});

var add10 = add(10);
console.log(add10(5));
console.log(add(5)(10));


function _curry(fn){
  return function(a,b){
    return arguments.length == 2
    ? fn(a,b)
    : function(b){ return fn(a,b) }
  }
}
// 원하는 시점까지 미뤄뒀다가 원하는 시점에서 실행하는 기법. 함수형 프로그래밍은 ㄹㅇㄹㅇ이렇게 조합해 나가는 것임.

console.log(add(10,20))
첫번째 실행때 인자가 2개면 바로 리턴으로 실행해버리는 코드.


var _get = _curryr(function (obj,key){
  return obj ==null? undefined: obj[key];
})
var user1 = users[0];
// console.log(user1.name); // 만약 user1이 없다면 에러가나게된다
console.log(_get(user1,'name')); // _get을 사용하게되면 undefinded을 반환하게 된다.

var [a,b] = [1,2];
[a,b] = [2*a,3*b];
console.log(a,b);
var array, first ,second;
array = [first,second] = [1,2,3,4];
console.log(array,first,second);
[a,b, ...rest] = [1,2,3,4];
console.log(a,b,rest);
[a=0, b=0, c=2] = [1,2];
console.log(a,b,c);
function rotation(x,y,theta){
  var s = Math.sin(theta), c = Math.cos(theta);
  return [c*x - s*y, s*x + c*y];
}
var [a,b] = rotation(1,2,Math.PI/3);
console.log(a,b)



```

