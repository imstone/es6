##箭头函数
现在函数可以用一个 => 箭头表示函数了。
需要注意的是 箭头函数内的this表示的是定义时候的上下文，而不是调用时候的上下文。

#### 介绍一下简单用法
```javascript
  // 表达式
  var list = [1, 2, 3, 4];
  
  var list2 = list.map(v => v+1);
  
  // 上面的代码就相当于
  list.map(function (v){
    return v + 1;
  })
  
  // 输出后是 [2, 3, 4, 5]
  var list3 = list.map((v, i) => v + i);
  // 输出结果是 [1, 3, 5, 7]

  // 函数体 大括号{}
  // 当代码逻辑有多行时候需要使用大括号吧代码包裹起来
  var array = [];
  list.forEach((item) => {
    if (item % 2 ===0 )
      array.push(item);
  })
  // 输出 [2, 4]
  
  // this 的特别说明
  // 在箭头函数内 没有this 箭头函数的this 就是定义时候的最外层的this；
  var team = {
    name: 'baidu',
    teamNumbers: ['li', 'zhang', 'zhao'],
    showAll() {
      this.teamNumbers.forEach(item => {
        console.log(this.name + item)
      })
    }
  }
  // 输出baiduli  baiduzhang   baiduzhao
  
  // 举一个极端点例子
  function testThis (){
    return () => {
      return () => {
        console.log( this.id);
      }
    }
  }
  



  
```


