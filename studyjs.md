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


