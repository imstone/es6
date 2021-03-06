#解构赋值

#### ES6对赋值给予了更多的方式；
可以给var let const赋值；

```javascript

var [a, b, c] = [1, 2, 3]
// 相当于 var a =1;
// var b =2;
// var c =3;

```
只要等号左右两侧的结构对应，就可以正确赋值；
如果左右不一致，也可以部分解构，左侧变量若果少会直接舍弃，如果左侧多会被赋值undefined
``` javascirpit

var [a ] = [1, 2]
// a ==1 
var [a, b] = [1]
// a ==1, b==undefined

```

#### 默认值
``` javascipt
var [a = '2'] = [];
// a === '2'
```

#### 对象的解构
我们上面的例子都是一些数组的例子，我们知道json。
对象其实也可是一种数据结构；


``` javascipt
var  {a, b} = {a: 1 ,b: 2};
// a
// 1
// b
// 2
```
与数组解构不也一样的是，数组解构需要注意的是顺序，而对象解构只要key值一样就可以正确赋值了。

#### 混合解构
既然数组和对象都可以解构赋值，那么两者结合一起呢？
当然也是可以的

``` javascipt
var  {a, d:[b, c]} = {a: 1 ,d: [2, 3]};
// a === 1
// b === 2
// c === 3
// d is not defined


```


#### 字符串解构

``` javascript

var [a, b, c, d, e] = 'nihao';
a // 'n'
b // 'i'
c // 'h'
d // 'a'
e // 'o'

```

#### 函数参数解构
``` javascirpt
function a ([a, b]) {
  return a + b
}

a([3, 4])
// 7

```


### 解构的用途


