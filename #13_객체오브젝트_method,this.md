# 객체 - method,this

## 1. method

- 객체 프로퍼티로 할당 된 **함수**

```
const superman = {
name : 'clark',
age : 33,
fly()  // : function()을 줄임
{
console.log('gogo')
}
}

superman.fly();
```

## 2. this



```
let boy={
name : 'Mike',
sayHello(){
  
console.log(this);
  
}
};

let girl ={
name : 'Jane',
sayHello(){
console.log(this.name);
}

};


boy.sayHello(); //name : Mike
girl.sayHello(); // Jane



```

1. **화살표를 사용 할 경우** 

```
let boy={
name : 'Mike',
sayHello:()=>{
  
console.log(this); //화살표를 사용 할 경우 this는 객체 변수가 아니라 전역 변수를 찾아감 따라서 에러가 뜸
  
}
};
boy.sayHello(); // error
```

