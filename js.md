# JavaScript #
## 1.js简介 ##
    JavaScript 为了解决服务器端语言。
    JavaScript，一种直译式脚本语言，是一种动态类型、弱类型、基于原型的语言，内置支持类型。它的解释器被称为 JavaScript 引擎，为浏览器的一部分，广泛用于客户端的脚本语言，最早是在 HTML 网页上使用，用来给HTML网页增加动态功能。然而现在 JavaScript 也可被用于网络服务器，如 Node.js。
## 2.js的组成 ##

	 ECMAScript ECMAScript是一种脚本语言的标准，ECMA-262标准。
	 BOM  全称：Browser Object Model，译为浏览器对象模型。
	 DOM  全称： Document Object Model，译为文档对象模型。

## 3.变量和常量 ##
    

	1. 变量
	
	      变量是存储数据信息的容器。变量被认为是有名字的容器。在代码中，使用变量名为值命名，需要遵守一定的规则。
	      在 JavaScript 代码中，使用变量前应当先声明。变量是使用关键字 var 声明的。 等号（=）是赋值运算符。
			命名规则：
			必须以字母、下划线（_）、美元符号（$）开始。
			不能以数字开头。
			不能使用关键字和保留字作为名称。
			由于 JavaScript 是区分大小写的，大写字母与小写字母并不冲突。
			名称最好有明确的含义。
			可以采用“下划线命名法”、“小驼峰命名法”或“大驼峰命名法” 之一，在开发团队内进行协调统一。
		
	
	2. 常量
		   常量就是一个只读（read-only）的变量。常量与变量类似，同样用于存储数据信息。只是常量的数据一旦被定义，便不能被修改。
		---在 ECMAScript 5 版本前，没有定义常量的语法。使用 var 关键字定义变量。
		---在 ECMAScript 5 版本后，提供了关键字 const 定义常量。
## 4.数据类型 ##



	  一、数据类型
         数据类型可分为可变类型和不可变类型。
			。可变类型的值是可修改的，对象和数据就属于可变类型.
			。不可变类型的值是不可修改的，数字、布尔值、null 和 undefined 都属于不可变类型。
	
	
	   二、原始类型
			分别为 boolean 类型、number 类型和 string 类型三种。
			有些资料将undefined 和 null 也归为原始类型（这里表示为特殊类型）。
		  1.布尔（boolean）类型
			         是指真或假、开或关、是或否。这个类型只有两个值：true 和 false。
				    	数据类型 转换为 true 的值 转换为 false 的值
		    			boolean类型 true false
		    			string类型 任何非空字符串   “”（空字符串）
		    			number类型 任何非零数字值（包括无穷大）  0和NaN
		    			object类型 任何对象null
		    			undefined undefined
		   2.number类型
			整数类型: 包括负整数、0和正整数等。
			浮点类型: 表示小数，JavaScript 中的所有数字均用浮点类型表示。
			   ** 1.浮点类型**
			      就是指该数值包含整数部分、小数点和小数部分。
			               --可以没有整数，但不推荐这种写法。
			              --保存浮点类型需要的空间是保存整数类型的两倍。
			   ** 2.四舍五入**
			         JavaScript通过浮点类型只能表示有限的个数在JavaScript中使用浮点类型时，常常只是真实值的  一个近似表示。
			   **3.NaN**
			      NaN（Not a Number），即非数值，是一个特殊的数值。
			          ----JavaScript提供了isNaN( )函数。该函数用于判断计算结果是否为数值。
						任何涉及NaN的操作都会返回NaN。
						NaN与任何值都不相等，包括NaN本身。
		3.string 类型
		4.typeof 运算符
		三、引用类型
		    在 JavaScript 中，对应原始类型提供了引用类型。通过引用类型可以创建原始类型的对象。
		    由于 JavaScript 是区分大小写的，从写法上来说，原始类型是全部小写，引用类型则是大写。
			  1.Boolean 类型是原始类型 boolean 类型对应的引用类型。
				boolean 类型与 Bollean 类型的区别:
					typeof 运算符对原始类型返回 "boolean"，而对包装类型为 "object"。
					instanceof 运算符测试 Boolean 类型返回 true，而测试 boolean 类型返回 false。
			  2.Number 类型是原始类型 number 类型对应的引用类型。
			          number 类型与 Number 类型的区别:
						typeof 运算符对原始类型返回 "number"，而对包装类型为 "object"。
						instanceof 运算符测试 Number 类型返回 true，而测试 number 类型返回 false。
			
		      3.String 类型是原始类型 string 类型对应的引用类型。
			       string 类型与 String 类型的区别:
					typeof 运算符对原始类型返回 "string"，而对包装类型为 "object"。
					instanceof 运算符测试 String 类型返回 true，而测试 string 类型返回 false。
		
			  4.instanceof 运算符
			      左侧的变量是右侧的数据类型，返回的是ture，否则false.
			         eg:
					var str = "this is message";
					str instanceof String;// 计算结果为 true, str是String类型
					str instanceof Object;// 计算结果为 true, 所有包装类型都是Object的实例
					str instanceof Number;// 计算结果为 false
			


	  5.undefined,undefined 类型只有一个值，就是 undefined。
	        下列情况会返回undefined:
					访问未修改的变量 undefined
					没有定义 return 表达式的函数隐式返回 undefined
					return 表达式没有显式的返回任何内容
					访问不存在的属性
					任何被设置为 undefined 值的变量
	  6.null 类型
	      null 类型是 JavaScript 中的一个特殊类型，用于表示一个不再指向任何内存空间地址的变量。
	      null 值多用于释放 JavaScript 中的资源（变量、数组和函数等）。
	  7.undefined与null 
	共同点: 都是原始类型，保存在栈中。
	不同点:
		undefined - 需要在内存中开辟空间进行存储
		null - 根本就不在内存中开辟任何空间
		         * 作用 - (从内存中)释放资源
> 注意: 所有对象都是 Object 类型的实例对象，通过 instanceof 运算符判断一个对象是否为具体数据类型，也包含"父类"。         
>    JavaScript 中有两个表示空的数据类型  undefined  null
## 5.类型转换 ##
    由于 JavaScript 是弱类型/松散类型的，在任何情况下都可以强制转换。
###1.隐式类型转换
#####转换为字符串
        将一个值加上空字符串可以轻松转换为字符串类型。
        eg:  '' + 10 === '10'; // true
#####转换为数字
        使用一元的加号操作符，可以把字符串转换为数字。
        eg:  +'10' === 10; // true
#####转换为布尔值
        使用否操作符两次，可以把一个值转换为布尔型。
        eg:  !!'foo'; // true
###2. 显式类型转换
####使用 JavaScript 的引用类型的构造函数进行类型转换。
	构造函数	     描述

	Number()	  将字符串或布尔值转换为数字，如果包含非法字符，则返回NaN。
	String()	  将数字或布尔值转换为字符串。
	Boolean()	  将字符串或数字转换为布尔值。
####使用数据类型的转换函数进行类型转换。

	构造函数	        描述
	toString()	    将数字或布尔值转换为字符串。
	parseInt()	    将字符串或布尔值转换为整数类型。
	parseFloat()	将字符串或布尔值转换为浮点类型。

