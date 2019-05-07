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



