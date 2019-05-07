typescript 语法笔记

类型：

let isDone:boolean = false;

数字

let decLiteral:number = 6;

let hexLiteral:number = 0xf00d;

let octalLiteral:number = 0x744;

字符串

let name: string = 'bob';

name = 'smith';

模板字符串

数组

let list:number\[\] = \[1,2,3\]

数组泛型

let list:Array&lt;number&gt; = \[1,2,3\];

元祖

let x:\[string,number\];

枚举

enum Color{Red,Green,Blue}

let c:Color = Color.Green;



let notSure:any = 4;

notSure = "maybe a string instead";

notSure = false;



let notSure:any = 4;

notSure.ifItExists\(\);

notSure.toFixed\(\);

let pretrySure:Object = 4;

prettySure.toFixed\(\);



let list:any\[\] =\[1,true,'free'\];

list\[1\] = 100;



function warnUser\(\):void{

console.log\("This is my warning message"\);

} 

不返回值

let unusable:void = undefined;

void类型的变量没有什么大用，因为你只能为它赋予undefined 和 null;

let u:undefined = undefined;

let n:null = null;

当你指定了 -- strictNullChecks 标记，null和undefined 只能赋值给void和他们各自。

这能避免很多常见问题。

Never ，never 类型表示的是那些永不存在的值得类型。

never 类型是任何类型的子类型，也可以赋值给任何类型；



Object 表示非原始类型，也就是除number,String,boolean,symbol,null 或者undefined之外的类型



类型断言 好比其他语言里的类型转换，但是还不进行特殊的数据检查和解构。

let someValue:any = 'this is a string';

let strLength:number = \(&lt;string&gt;someValue\).length;



let someValue:any = 'this is a string";

let strLength:number = \(someValue as string\).length;









关于let







