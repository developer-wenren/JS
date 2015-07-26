#JS应用类型
---
##Object类型
* 通过`new`创建的Object类型的实例对象
 >var person = new Person();
* 使用字面量表示法定义对象
>var person = { name:"Kity", age: 21}

---
##Array类型
* 如何创建一个数组

		var colors = new Array();
		var colors = var colors = new Array();
		var colors2 = new Array('yellow','red', 'gray');
		var colors3 = Array('yellow', 'red');
		var color4 = ['yellow', 'red'];
		var color5 = [ ];
* 常用属性和方法
				
		length 获取长度
		isArray 判断是否为数组
		toString, valueOf 转换其他类型
		push(), pop() 栈方法操作
		shift(), unshift()正反队列操作
		sort(), reverse() 排序方法操作
		concat(), slice() 添加,裁剪操作
		indexOf() 获取索引
		every(), forEach(), map(), filter()迭代操作
		reduce(),reduceRight() 缩小操作
---
##Date类型
*获取日期
> var date = new Date();

> var dateString = Date.parse();

*常用方法

	toDateString()
	toTimeString()
	toLocaleDateString()
	getTime()
	getFullyear()
	...
---
##RegExp类型

* 创建方式
	
	var exp2 = new RegExp("[bc]at", "i");
	var exp = / pattern / flags ;
	flags:
		* g 全局
		* i 忽略大小写
		* m 多行
			// 所有含at的字符串
				var pattern1 = /at/g;
			// 第一个bat或cat,不区分大小写
				var pattern2 = /[bc]at/i;
			// 匹配所有以'at'结尾的3个字符,不区分大小写
				var pattern3 = /.at/gi;

* 使用方法
	
		exec(text) 
		match.index
		match.input
		...
---
#Function类型

* 每个函数都为Function类型的实例, 函数名实为指向Function类型对象的指针
* 为什么JS没有函数重载 (函数名 指针)
	
		function addSomeNumber(num) { 
			return num + 100;
		}
		function addSomeNumber(num) {
    		return num + 200;
		}
		var a = addSomeNumber(300);
		console.log(a);
		//------------------
		var addSomeNumber2 = function(num) {
    	return num + 100;

		}
		addSomeNumber2 = function(num) {
    	return num + 200;
		}

		var result = addSomeNumber2(300);
		console.info(result);

* 函数内部属性
	* 特殊对象 `arguments`, `this`
		1. `arguments` 类数组参数: 保存函数参数.

				callee 属性: 一个指向所属函数的指针
				用法: 
				function factorial(num) { 
				if(num<=1) {
        				return 1;
    			}else {
    			    return num * arguments.callee(num-1);
					}	
				}
		2. `this` 当前函数数据所执行对象, 全局函数的`this`为`Window`

* 函数属性、方法
	1. apply(obj, args)

			function sum(num1, num2) {
    			return num1 + num2;
			}
			function callSum1(num1, num2) {
    			return sum.apply(this, arguments);
			}
			function callSum2(num1, num2) {
    			return sum.apply(this, [num1,num2]);
			}
			console.info(callSum1(10, 20));//30
			console.info(callSum2(20, 10));//30
	2. call(obj, arg1, agr2,...)

			function add(n1, n2) {
    			return n1 + n2;
			}
			function callAdd(n1, n2) {
				return sum.call(this, n1, n2);

			}
			console.info(callAdd(1, 3));//4
	3. call()和apply()重用

			window.color ='red';
			var o = {color: 'blue'};
			function sayColor() {
				console.info(this.color);
			}
				sayColor(); // red	
				sayColor(color11); //red		
				sayColor(window); //red
				sayColor.call(o)  // blue	
---
#Global对象
* 特殊对象方法: `isNaN()`, `parseInt`, ...

* URL编码方法
	* encodeURL( ) 全段URL编码处理
	* encodeURLComponet( ) 某段URL编码处理
	* decodeURL( ) 全段解码
	* decodeURLComponet( ) 某段解码

* eval( ) 方法

* 特殊属性: Array, String, Boolean, Eorror, ...

* window 对象

* Math 对象

		常用方法
		Math.PI; // 3.1413...
		Math.min(...);
		Math.max(...);
		Math.round() //四舍五入
		Math.random()// 0~1随机
		Math.abs() //绝对值