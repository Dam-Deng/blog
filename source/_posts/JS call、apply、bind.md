title: JS call、apply、bind
date: 2017-08-15 12:13:22
author: dam
tags: this

---
# a.call(thisArgs ,arg1, arg2, arg3)
* 不传，或者传null,undefined， 函数中的 this 指向 window 对象
* 传递另一个函数的函数名，函数中的 this 指向这个函数的引用
* 传递字符串、数值或布尔类型等基础类型，函数中的 this 指向其对应的包装对象，如 String、Number、Boolean
* 传递一个对象，函数中的 this 指向这个对象

```
// 一些类数组对象就可以用这些办法来遍历：
Array.prototype.forEach.call(arguments, function(i){
    console.log(i)
});
// 其中arguments就是函数的参数
```

# a.apply(thisArgs, [arg1, arg2, arg3])
```
var arr = [2,3,1,5,4];
Math.max.apply(null,arr); // 求数组的最大值 5
```

# a.bind(thisArgs, arg1, arg2, arg3)
bind了之后不会马上执行函数， bind了之后再调用call或者apply也不会有效


# callee
callee是返回正在被执行的function函数，也就是所指定的function对象的正文。
__argument.callee()表示fn()__
```
var result=[];
function fn(n){  //典型的斐波那契数列
   if(n==1){
        return 1;
   }else if(n==2){
           return 1;
   }else{
        if(result[n]){
                return result[n];
        }else{
                //argument.callee()表示fn()
                result[n]=arguments.callee(n-1)+arguments.callee(n-2);
                return result[n];
        }
   }
}
```

# caller
caller是返回一个对函数的引用，该函数调用了当前函数；
```
var a = function() {   
    console.log(a.caller);   // 输出b的值
}   
var b = function() {   
    a();   
}   
b(); 
```
