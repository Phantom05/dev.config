###  # 1. undefined와 null 의 차이점에 대해 기술하시오.

#### **null**

+ null은 비어있거나 존재하지 않는 value를 나타낸다
+ null은 할당되어야 존재할 수 있는 값이다.(기본적으로 주어질 일은 없다)
+  null의 type을 체크하는 테스트를 진행해보면 object를 리턴한다.
+  숫자문맥에서는 0으로 변환되고, 문자열문맥에서 사용하게되면 "null"로 변환된다.

#### **undefined**

+ undefined는 주로 선언된 변수지만 값 할당이 이루어지지 않았음을 나타낸다. 객체 프로퍼티도 마찬가지.
+ 존재하지 않는 값을 찾게 되어도 undefined를 뱉는다.
+  숫자문맥에서는 NaN으로 변환되고 문자열문맥에서 사용될경우에는 "undefined"로 변환된다.



```js
let logHi = (str = 'hi') => {
  return str
}

logHi(undefined)  // hi
logHi(null) // null

null = 'hello' // ReferenceError
undefined = 'value' // 'value'
```







## # 2. var, const, let에 대해 설명하시오.



> 설명하기 앞서, 변수의 실행컨택스트는 기본적으로 3단계를 거쳐 생성이된다.

+ **선언 단계(Declaration phase)**
  + 변수를 실행 컨텍스트의 변수 객체(Variable Object)에 등록한다. 이 변수 객체는 외부 렉시컬 환경 컴포넌트 참조가 참조하는 대상이 된다.
+ **초기화 단계(Initialization phase)**
  + 변수 객체(Variable Object)에 등록된 변수를 위한 공간을 메모리에 확보한다. 이 단계에서 변수는 undefined로 초기화된다.
+ **할당 단계(Assignment phase)**
  + undefined로 초기화된 변수에 실제 값을 할당한다.



**var 키워드로 선언된 변수는 선언 단계와 초기화 단계가 한번에 이루어진다.** 즉, 스코프에 변수를 등록(선언 단계)하고 메모리에 변수를 위한 공간을 확보한 후, undefined로 초기화(초기화 단계)한다. 따라서 변수 선언문 이전에 변수에 접근하여도 스코프에 변수가 존재하기 때문에 에러가 발생하지 않는다. 다만 undefined를 반환한다. 이후 변수 할당문에 도달하면 비로소 값이 할당된다. 이러한 현상을 **변수 호이스팅(Variable Hoisting)**이라 한다.

<hr>

#### **var**

`var`는 코드의 문맥과 잘 맞지 않는 동작을 하기 때문에, **쓰지 않을 수 있다면 쓰지 않는 것이 좋습니다.** 변수를 선언할 때에는 `const`를 가급적 사용하고, 변수에 다른 값을 대입해야 할 일이 생기면 그 때에만 `let`을 사용합니다.

`var`같은 경우 선언과 동시에 글로벌 렉시컬 컴포넌트 함수객체로 1,2단계를 거쳐 메모리 할당이 이루어 집니다. 때문에 아래 1#에서 동작하는 코드는 사실상 #2와 같습니다.

동일한 글로벌 렉시컬 환경 컴포넌트의 함수객체에서 참조하는 것이기 때문에 계속하여 재할당이 됩니다. 이는 렉시컬 네스팅이 조금만 복잡해져도 익숙하지 않을경우 실수를 자주 범하기도 합니다.

즉, 함수스코프로 사용되기 때문에, 계속하여 참조되고 덮혀 쓰여지는 것입니다.

```js
//#1
let ecount =10;
var a = 10
var b = 12
var a = 20


//#2
var a;
var b;

let ecount =10;

a=10
b=12
a=20

// 스코프의 선두에서 선언 단계와 초기화 단계가 실행된다.
// 따라서 변수 선언문 이전에 변수를 참조할 수 있다.
console.log(foo); // undefined

var foo;
console.log(foo); // undefined

foo = 1; // 할당문에서 할당 단계가 실행된다.
console.log(foo); // 1

```

위와 같이 스크립트가 실행과 동시에 자동적으로 글로벌 렉시컬 환경 컴포넌트 안쪽으로 할당이 되기 때문에 아래와 같은 코드를 사용할떄 참조에러 `ReferenceError` 가 나지 않습니다.

```js
console.log(hello) // undefined
var hello = 10;
```

또한 함수 렉시컬 컴포넌트 네스팅으로 인해 참조에 주의하지 않으면 의도치 않은 동작을 하게됩니다.

```js
for (var i = 0; i < 3; i++) {
  console.log('outer');
  // 위아래 두 `i` 변수는 같은 함수 스코프에서 정의된 같은 변수입니다.
  // 바깥쪽 루프를 한 번 도는 동안, 안쪽 루프를 도느라 이미 `i`의 값이 3이 되어버렸습니다.
  // 같은 i값을 참조하고 있기 때문에 안쪽반복문에서 3이 됨과 동시에 위쪽의 함수가 종료되어 버렸습니다.
  for (var i = 0; i < 3; i++) {
    console.log('inner');
  }
}
```

또한, for라는 함수의 환경 컴포넌트 안쪽으로 다시 for함수가 실행 되었기 때문에, 내부 함수 환경 컴포넌트로 적용되어 같은 환경 컴포넌트의 위치에 있기 때문에 같은 i 값을 참조하게 되기 때문입니다.





#### **const**

`const` 는 블록레벨 스코프입니다. 블록레벨 스코프의 경우, `{}`안쪽의 선언된 변수는 블록 내에서만 유효하며, 코드 블록 외부에서는 참조할 수가 없습니다. `const`는 상수(변하지 않는 값)를 위해 사용합니다. 하지만 반드시 상수만을 위해 사용하지는 않습니다. const의 특징은 let과 대부분 동일하므로 let과 다른 점만 살펴보도록 하겠습니다.

+ let은 재할당이 자유로우나 const는 재할당이 금지됩니다.
+ 주의할 점은 **const는 반드시 선언과 동시에 할당이 이루어져야 한다**는 것이다. 그렇지 않으면 다음처럼 문법 에러(SyntaxError)가 발생합니다.
+ const는 let과 마찬가지로 블록 레벨 스코프를 갖습니다.
+ const에 객체나 배열을 할당할경우 객체나 배열 자체를 할당한것이지 안의 프로퍼티들까지 보호해주진 않습니다. 이는 object를 참조하는 것이기 때문에 object자체를 재할당 하지 않는이상 프로퍼티의 수정은 허용합니다.





#### **let**

`let` 는 블록레벨 스코프이다. 블록레벨 스코프의 경우, `{}`안쪽의 선언된 변수는 블록 내에서만 유효하며, 코드 블록 외부에서는 참조할 수가 없다. 또한 전역에서 선언하더라도, 사실상 window객체 내에 선언된것이 아니라, let의 고유한 블록스코프 내에 존재한다. 

```js
let foo = 123; //무늬만 전역변수
window.foo // undefined
```



**let 키워드로 선언된 변수는 선언 단계와 초기화 단계가 분리되어 진행된다.** 즉, 스코프에 변수를 등록(선언단계)하지만 초기화 단계는 변수 선언문에 도달했을 때 이루어진다. 초기화 이전에 변수에 접근하려고 하면 참조 에러(ReferenceError)가 발생한다. 이는 변수가 아직 초기화되지 않았기 때문이다. 다시 말하면 변수를 위한 메모리 공간이 아직 확보되지 않았기 때문이다. 따라서 스코프의 시작 지점부터 초기화 시작 지점까지는 변수를 참조할 수 없다. 스코프의 시작 지점부터 초기화 시작 지점까지의 구간을 ‘일시적 사각지대(Temporal Dead Zone; TDZ)’라고 부른다.

```js
// 스코프의 선두에서 선언 단계가 실행된다.
// 아직 변수가 초기화(메모리 공간 확보와 undefined로 초기화)되지 않았다.
// 따라서 변수 선언문 이전에 변수를 참조할 수 없다.
console.log(foo); // ReferenceError: foo is not defined

let foo; // 변수 선언문에서 초기화 단계가 실행된다.
console.log(foo); // undefined

foo = 1; // 할당문에서 할당 단계가 실행된다.
console.log(foo); // 1
```

![let-lifecycle](https://user-images.githubusercontent.com/33567964/57579749-8afce480-74db-11e9-910b-5123c9af41ef.png)


**요약 표**

|           | const | let   | var      |
| :-------- | ----- | ----- | -------- |
| 스코프    | block | block | function |
| 재대이    | X     | O     | O        |
| 재선언    | X     | X     | O        |
| 호이스팅  | X     | X     | O        |
| 사용 권장 | 1순위 | 2순위 | 3순위    |



### # 3. function Person(){}, var person = Person(), and var person = new Person() 위 세가지 코드의 차이점에 대해 기술하시오.

위 3가지 함수 객체 코드는 함수 선언문, 표현문, 인스턴스 생성에 대한 코드입니다. 선언문의 경우 자바스크립트 엔진이 런타임과정에서 할당과 동시에 호이스팅 되며, 전역 렉시컬 환경 컴포넌트에 바인딩 됩니다.  하지만 함수 표현문은 호이스팅은 되지만 할당은 되지 않습니다. 

### function Person(){} vs var person = Person()

```js
//선언문
foo();
function foo() {
    console.log('hello');
};
> hello

// 표현문
poo; // undefined
var poo = function() {
    console.log('hello');
};

foo(); // foo is not a function
var foo = function() {
    console.log('hello');
};
```



### var person = new Person()

new 의 경우 Person함수의 인스턴트를 만들어주는 빌트인 객체이며, 동작방식은 아래와 같습니다.

```js
let newObj = {};
newObj.__proto__ = Person.prototype;
Person.apply(newObj, arguments);
return newObj
```

새로 생성될 객체의 prototype Link 로 Person의 prototype Object를 참조하게 되고, apply로 new 로 생성될떄 들어온 Person의 인수들을 newObj로 this bind 해줍니다. 그리고선 새로운 객체를 리턴하여 var person으로 할당해주는 것입니다.





### #4. 함수의프로퍼티와 프로토타입에 관해 기술하시오. 

### function ecount(){} ecount.name = "이카운트"; //property ecount.prototype.name = "ECOUNT";  //prototype



**ecount.name**의 경우 자바스크립트에서 함수의 경우 사실상 함수 객체에서 사용되는 거기 때문에 여느 객체와 마찬가지로 닷노테이션으로 프로퍼티를 선언할 수 있습니다. 때문에 function ecount(){}의 경우 객체로 동작되기 때문에 ecount.key = value로 동작될 수 있는것이고, 함수자체가 생성될떄, `prototype` 객체와 `length`, `caller`,` name`,`argument`와 `[[scope]]`객체가 생성되게 됩니다. 



**ecount.prototype.name**의 경우 함수 오브젝트를 선언할때, 컨스트럭트로 생성되기 때문에 `__proto__` 인 prototype link 객체가 아닌 prototype Object object 를 갖게 됩니다. 때문에 prototype객체안에 name을 생성되게 되고 이는 new 지시자로 인스턴스를 생성하게 될때 `__proto__`로 참조하게 되는 대상 객체가 됩니다.  때문에

```js
let basicQuestion = new ecount();
console.dir(basicQuestion)

> ecount
  >__proto__:
    >constructor: ƒ ecount()
    >__proto__: Object
```

이런 그림이 되고, 컨스트럭트 객체는 prototype 으로 자기 자신을 참조하고 있기떄문에 이는 순환 참조가 되게 됩니다. 또한 인스턴스에서는 컨스트럭트의 일반 property 에는 접근하기가 힘들기 때문에 prototype 패턴을 자주 사용하게 됩니다.





### # 5. `__proto__`와 `prototype`에 대해 기술 하시오 (프로토타입을 이용한 상속 모델 구현의 관점에서 기술하시오)

둘의 차이는 위에서부터 계속 사용된 개념입니다. 자바스크립트가 동작하기 위해 Web api 와 콜스택, 이벤트루프, 테스트큐, 실행 컨택스트가 사용되며, Object object위 쪽으론 [native code]가 실행되게 됩니다.  떄문에 5번에선 프로토타입의 기본적인 동작을 설명하겠습니다. 프로토타입은 기본적으로 상속의 개념이며, prototype link 인 `__proto__`를 타고 컨스트럭트의 prototype object 객체를 참조하게 됩니다. 인스턴스에서 특정한 프로퍼티를 사용할때 기본적이로 해당 인스턴스의 객체를 훑고 없을시 `__proto__`로이동하여 해당 프로퍼티를 찾게 됩니다. 이 `__proto__`는 constructor의 prototype Object 객체라고 볼수 있으며,해당 객체에 없을시 construct의 객체의 `__proto__`로 이동하여 더 상위인 Function Object의 prototype Object 객체를 훑습니다. 이때도 만약 원하는 프로퍼티가 있으면 해당 값을 반환할 것이고, 해당 값이 없을시 다시 Function Object의 `__proto__`로 들어가게 됩니다 이때 참조하는 prototype Object는 Object object의 `__proto__` 이며, 해당 객체에서도 프로퍼티가 있으면 반환합니다. 하지만 Object object에서 찾지 못할경우 undefind를 반환하게 됩니다.





### #6. apply, call 함수의 공통점과 차이점에 대해 기술하시오.

apply와 call은 this 바인딩을 컨트롤 해주는 메서드입니다. apply 앞쪽의 함수의 프로토타입의 메서드에서 apply를 동작시켜, 첫번째 인자로 this를 타겟으로 바인딩 해주고 두번째 인자로 값을 넣어 동작시키는 메서드입니다. 위쪽의 new 를 생성할때 apply를 사용하였는데 call과 다른점은 인자를 배열로 받는다는 점입니다.

```js
type = "poo";
var type1 = { type: "one" };
var type2 = { type: "two" };
 
function getType() {
    console.log(this.type); // es5의 선언식 함수내부에서의 this는 window에 this를 바인딩함.
}
 
getType(); // 전역 객체의 type 타겟
getType.call(this);// 전역 객체의 type 타켓
getType.call(type1); // type1객체에 this 바인딩, type1.type인 one 타겟
getType.call(type2); // type1객체에 this 바인딩, type2.type인 two 타겟

const bruce = { name : 'Bruce'};
const madeline = { name : 'Madeline'};

function update(birthYear, occupation){
   this.birthYear = birthYear;
   this.occupation = occupation;
};
update.call(bruce, 1949, 'singer'); // this바인딩 bruce로 변경
update.call(madeline, 1942, 'actress'); // madeline 변경

```

+ 특이한점은 apply는 유사배열인 arguments까지 취급할 수 있다는 점입니다.



### #7. bind 함수를 구현하시오. Function.prototype.bind = function(){}

```js
Function.prototype.bind = function (obj) {
  if (!obj) return this;
  return (...args) => this.apply(obj, args);
};
```



### #8. 아래의 코드가 실행되도록 add(item, index) 함수를 구현하시오. (splice 함수 사용하지 말 것) [1,2,3].add("c",1);          //[1,"c",2,3];

```js
Array.prototype.add = function(tar,idx){
  let res = this.slice(idx);
  res.unshift(tar);
  return this.slice(0,idx).concat(res);
};
```



### #9. MVVM 패턴에 대해 설명하시오.

### Model + View + ViewModel

MVVM은 두가지 디자인 패턴을 사용합니다. 바로 Command패턴과 Data Binding 인데요. 이 두가지 패턴으로 인해 View와 ViewModel은 의존성이 완전히 사라지게 됩니다. MVP와 마찬가지로 View에서 입력이 들어오구요. 입력이 들어오면 Command 패턴을 통해 ViewModel에 명령을 내리게 되고 Data Binding으로 인해 ViewModel의 값이 변화하면 바로 View의 정보가 바뀌어져 버리게 됩니다.

**Data Flow Stream**

1. View에 입력이 들어오면 Command 패턴으로 ViewModel에 명령을 합니다.
2. ViewModel은 필요한 데이터를 Model에 요청 합니다.
3. Model은 ViewModel에 필요한 데이터를 응답 합니다.
4. ViewModel은 응답 받은 데이터를 가공해서 저장 합니다.
5. View는 ViewModel과의 Data Binding으로 인해 자동으로 갱신 됩니다.



### #10. 클로저에대해 설명하시오.

클로저(closure)는 쉽게 말하면, 내부함수가 외부함수의 맥락(context)에 접근할 수 있는 것을 가리킵니다. 언어적인 관점에서 설명하자면, 자기 자신이 정의된 환경에서 함수 안에 있는 자유 변수의 식별자 결정을 실행합니다. 즉 ,실행 컨택스트가 구성 될때, 렉시컬 환경이 구성되는데, 이 때 생성 된 렉시컬 환경 컴포넌트에서 외부 렉시컬 환경 컴포넌트 참조를 이용해 값을 참조하고 이때 참조를 하고 있기 때문에 가비지 컬렉션 대상이 되지 않습니다. 그러하여 해당 렉시컬 컴포넌트는 메모리 해제가 일어나지 않고 계속 살아있게 되며, 클로저를 이용하여 외부 함수 렉시컬 컴포넌트에 접근하여, 다양한 패턴을 이용할 수 있는 것입니다.   **참고**( es6부터는 가비지 컬렉션의 고립된 순환참조를 해결하기위해 window object에서 참조 가능한 상황만 가비지 컬렉션에서 제외됩니다.) 

클로저 예를 들어 보겠습니다.

```js
function makeCounter(){
    let count = 0;
    return f;
    function f(){
        return count++'
    }
}
let counter = makeCounter()
```

1. 위의 코드의 경우 외부함수 makeCounter는 중첩함수 f의 참조를 반환하게 됩니다.

2. 중첩 함수 f는 외부함수 makeCounter의 지역변수 count를 참조합니다.
3.  1번 상황으로 인해, f의 함수 객체를 전역 변수 counter가 참조합니다. 그 결과 함수 makeCounter의 렉시컬 환경 컴포넌트를 전역변수 counter가 f의 함수 객체로 간접적으로 참조히게 되므로 가비지 컬렉션이 대상이 되지 않고, 따라서 makeCounter  실행이 끝나서 호출자에게 제어권이 넘어가도 makeCounter의 렉시컬 환경 컴포넌트가 메모리에서 지워지지 않게 됩니다. 지역 변수 count는 함수 makeCounter가 속한 렉시컬 환경 컴포넌트에 있는 선언적 환경 레코드의 프로퍼티이므로 이 또한 메모리에서 지워지지 않습니다.
4. 이렇게 클로저 함수를 counter 변수에 반환 시켜 놓았을때, makeCounter의 지역변수 count는 외부에서 접근할 수가 없습니다. 이는 마치 접근자 프로퍼티 getter와 같다는 생각이 듭니다. 다른말로는 객체 프로퍼티는 외부로부터 은폐하는 행위를 캡슐화라고 하기 때문에 클로저는 캡슐화된 객체 라고 할 수 있습니다.
5. 특장점은 makeCounter함수를 실행 할때마다 새로운 렉시컬 환경 컴포넌트가 새로 생성되기 때문에, 각 클로저는 서로 다른 내부 상태를 저장하게 됩니다. 클로저를 객체로 간주하면 makeCounter는 클로저라는 객체를 생성하는 팩토리함수로 간주할 수 있습니다.

