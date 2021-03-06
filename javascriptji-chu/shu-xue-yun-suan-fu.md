# 数学运算符

#### 本节学习目标

* 掌握JS中的数学相关的运算符，`+`，`-`，`*`，`/`，`+=`……
* 能够用JS中的数学运算符进行数学运算

#### 本节内容

通过之前的学习，我们知道变量可以用来存储信息，包括字符串，数字等。本节我们所要学的是如何用JS实现基本的数学运算。

先做一道简单的数学题：“我们有15个苹果，20个梨，那么我们一共有多少个水果？”。答案是35个，那么我们如何用程序表示这道题呢？如下：

```JavaScript
var apple = 15;
var pear = 20;
var fruit = apple + pear;
alert(fruit); // 35
```

首先声明一个变量存储苹果的数量（`var apple = 15;`），再声明一个变量存储梨的数量（`var pear = 20;`）,最后声明一个变量用来存储水果的数量，并将它初始化为苹果和梨的数量之和（`var fruit = apple + pear;`）,那么`fruit`就存储了我们计算出来的水果的数量，这里的加号（`+`）表示和数学里相同的含义即相加。

首先先介绍一下赋值操作符，也就是等号`'='`，在JS中一个等号意为赋值，就是将等号右侧的值赋值给等号左侧的值。这里容易困惑的是赋值和判断相等的区别，一个等号代表赋值，若我们想判断`a`是否和`b`相等，则需要用`===`或`==`来判断，关于`===`和`==`的区别，简单来说就是三个等号是严格相等，既包含值的相等也包含数据类型的相等；但两个等号的相等只简单判断值，不判断数据类型；举个例子：

```JavaScript
alert('0' === 0); // false 严格相等判断，’0‘是字符串，而0是数字，故不严格相等。
alert('0' == 0); // true 非严格相等判断，会将’0‘隐式转换为0，再比较，即 0==0，故返回true。
```

在JS中和数学相关的操作符有这些：

* `'+'`：
  加。示例：
  ```JavaScript
  var x = 5;
  var result = x + 5;
  alert(result); // 10
  ```
* `'-'`：
  减。示例：
  ```JavaScript
  var x = 5;
  var result = x - 5;
  alert(result); // 0
  ```
* `'*'`：
  乘。示例：
  ```JavaScript
  var x = 5;
  var result = x * 5;
  alert(result); // 25
  ```
* `'/'`：
  除。示例：
  ```JavaScript
  var x = 5;
  var result = x / 2;
  alert(result); // 2.5
  ```
* `'%'`：
  取模。这里取模的意思其实就是求余数，比如：10除以3得3余1，那么10对3求模就是1。示例：
  ```JavaScript
  var x = 5;
  var result = x % 2;
  alert(result); // 1
  ```
* `'++'`：
  自加。这里自加意为将自己的值加一，比如：3自加之后就是4。示例：
  ```JavaScript
  var x = 5;
  x++;
  alert(x); // 6
  ```
* `'+='`：  
  加等。示例：

  ```JavaScript
  var x = 5;
  x += 2; // x = x + 2;
  alert(x); // 7
  ```

  加等就是将当前变量的值加上右侧的值，再赋值给当前值。比如上例中，`x += 2;`就是将`x`的值加上`2`在赋值给`x`。

* `'--'`：  
  自减。这里自减意为将自己的值减一，比如：4自减之后就是3。示例：

  ```JavaScript
  var x = 5;
  x--;
  alert(x); // 4
  ```

* `'-='`：  
  减等。示例：

  ```JavaScript
  var x = 5;
  x -= 2; // x = x - 2;
  alert(x); // 3
  ```

  减等就是将当前变量的值减去右侧的值，再赋值给当前值。比如上例中，`x -= 2;`就是将`x`的值减去`2`在赋值给`x`。

* 优先级  
  我们在数学中进行数学计算的时候，会有不同的优先级规则。比如：先算乘除，再算加减；有括号要先算括号里面的。这些规则在JS中进行数学运算是同样适用。示例：

  ```JavaScript
  alert(2 + 3 * 3);  // 11
  alert((1 + 2) * 2 + 2); // 8
  alert((2 + 2) / 2); // 2
  ```

  #### 其他资料推荐

* [JS表达式和操作符 - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators)
* [JS操作符 - w3school](https://www.w3schools.com/jsref/jsref_operators.asp)
* [JS中==和===的区别](https://appendto.com/2016/02/vs-javascript-abstract-vs-strict-equality/)
* [运算符优先级 - MDN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_Precedence)
  #### 本节练习

* 自己搜索查询`num++`（后面自加）和`++num`（前面自加）的区别，并进行总结。
* 自己搜索查询如何利用`Math`方法对得到的结果进行保留两位小数，四舍五入，向上取整，向下取整等操作，并进行总结。



