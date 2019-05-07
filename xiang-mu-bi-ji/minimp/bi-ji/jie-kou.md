接口是如何工作的

function printLabel\(labelledObj:{label:string}\){

console.log\(labelledObj.label\);

}

let myObj ={size:10,label:'size 10 Object'};

printLabel\(myObj\);

可选属性

```
interface SquareConfig{
color?:string;
width?:number;
}

function createSquare(config:SquareConfig):{color:string;area:number}
{
    let newSquare ={color:'white',area:100};
    if(config.color){
        newSquare.color = config.color;
    }
    if(config.width){   
        newSquare.area = config.width*config.width;
    }
    return newSquare;
}
let mySquare = createSquare({color:'black'});




 你可以在属性名前用 readonly来指定只读属性:
```

readonly vs const

最简单判断该用readonly还是const的方法是要看把它作为变量使用还是作为一个属性。作为变量使用的话用const，作为属性则使用readonly。

类型断言 as 。。。。

let mySearch:SearchFunc;

mySearch = function\(src,sub\){

let result = src.search\(sub\);

return result &gt;-1;

}

可索引的类型

a\[10\] ageMap\['daniel'\];

interface StringArray{

\[index:number\] :string;

}

let myArray:StringArray;

myArary = \['bob','fred'\];

let myStr :string = myArray\[0\];

TypeScript 支持两种索引签名，字符串和数字，

实现接口

```
interface ClockInterface{
currentTime:Date;
}
class Clock implements ClockInterace{
    currentTime:Date;
    constructor(h:number,m:number){}
}


interface ClockInterface{
    curerntTime:Date;
    setTime(d:Date);
}

class Clock implements ClockInterace{
    currentTime:Date;
    setTime(d:Date){
        this.currentTime = d;
    }
    constructor(h:number,m:number){}
}
```

类静态部分，和实例部分的区别

继承接口

接口继承接口

可以继承多个接口，创建出多个接口的合成接口

混合类型

interface Counter{

\(start:number\):string;

interval:number;

reset\(\):void;

}

function getCounter\(\):Counter{

let counter = &lt;Counter&gt;function \(start:number\){};

counter.interval = 123;

counter.reset = function\(\){};

return counter;

}

let c = getCounter\(\);

c\(10\);

c.reset\(\);

c.interval=5.0;

接口继承类

当接口继承了一个类类型时，它会继承类的成员但不包括扩其实现，

接口同样会继承到类的private和protected成员

这个接口类型只能被这个类或其子类所实现。

```
class Control{
    private state:any;
}
interace SelectableControl extends Control{
    select():void;
}
class Button extends Control implements SelectableContro{
    select(){}
}
class TextBox extends Control{
    select(){}
}
class Image implements SelectableControl{
    select(){}
}
class Location{


}
```



