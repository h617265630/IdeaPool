let和const

const 是对let 的一个增强，它能阻止对一个变量再次赋值

作用域规则

## 块作用域

当用`let`声明一个变量，它使用的是_词法作用域_或_块作用域_。 不同于使用`var`声明的变量那样可以在包含它们的函数外访问，块作用域变量在包含它们的块或`for`循环之外是不能访问的。

重定义以及屏蔽

用let 定义时

// 错误，不能在1个作用域里多次声明\`x\`

在一个嵌套作用域里引入一个新名字的行为称作屏蔽

```
for (let i = 0; i < 10 ; i++) {
    setTimeout(function() {console.log(i); }, 100 * i);
}
```

不仅在循环里引入一个新的变量环境

而是针对每次迭代都会创建一个新作用域。

const 声明

const 声明是声明变量的另一种方式。

const 引用的值是不可变的。



**结构数组**

数组结构赋值

let input = \[1,2\];

let \[first,second\] = input;

console.log\(first\);

console.log\(second\);

first = input\[0\];

second = input\[1\];

\[first,second\]  = \[second,first\];

function f\(\[first,second\]:\[number,numer\]\){

console.log\(first\);

console.log\(second\):

}

let \[first\] = \[1,2,3,4\];

console.log\(first\);

let \[,second,,fourth\] = \[1,2,3,4\];



let o = {

a:'foo',

b:12,

c:'bar'

};



\({a,b} = {a:'baz',b:101}\);



let {a,...passthrough} = o;

let total = passthrough.b +passthrought.c.length;



默认值

function keepWholeObject\(wholeObject:\[a:string,b?:number}\){

let{a,b=1001} = wholeObject;

}



函数声明

type C = {a:string,b?:number}

function f\({a,b}:C\):void{



}



function f\({a="",b=0}={}\):void{}

f\(\):



展开

展开允许你将一个数组展开为另一个数组，或将一个对象展开为另一个对象。

let first = \[1,2\];

let second = \[3,4\];

let bothPlus =\[0,...first,...second,5\];



let defaults = {food:'spicy',price:'$$',ambiance:'noisy'};

let search = {...defaults,food:'rich'};



大体上是说当你展开一个对象实例的时候，你会丢失其方法。

```
class C{
    p=12;
    m(){
    }
}
let c = new C();
let clone = {...c};
clone.p;
clone.m();

```



