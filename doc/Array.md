#数组
##数组拼接可以用[...[1,2,3], ...[4,5,6]] => [1,2,3,4,5,6].

### 把各个数组拆解然后拼接到一起返回一个新数组

##数组循环

```javascript
let arrayLike = {
    '0': 'a',
    '1': 'b',
    '2': 'c',
    length: 3
};

// ES5的写法
var arr1 = [].slice.call(arrayLike); // ['a', 'b', 'c']

// ES6的写法
let arr2 = Array.from(arrayLike); // ['a', 'b', 'c']
```

##数组过滤填充查找元素
