# ES6相关 #
1. let 、var 和 const  
   let 类似于 var ,但有不同：
		let 不存在变量的提升  
	const 声明变量和 let 声明变量类似，不同：const 声明的变量只可以在声明时赋值，不可随意修改。const只是保证变量名指向的地址不变，并不保证该地址的数据不变。const 可以在多个模块中共享。

2. 模板字符串  
  原来：let name = '名字：'+name+',今年'+age+'岁。  
  模板：let name =`名字:${name},今年${age}岁。`


3. flat() 和 flatMap()   
   Array.prototype.flat()用于将嵌套的数组“拉平”，变成一维数组。该方法返回一个新数组，对原数据没有影响。  如果原数组有空位，flat()方法会跳过空位。
	[1,2,3，[4],[[5],6]].flat(2) // flat()的参数为2，表示要拉平两层的嵌套数组。  
	[1, 2, 3, 4, 5, 6]  
	如果多层嵌套，转成一维数组，可以用Infinity关键字作为参数。  
	[1, [2, [3]]].flat(Infinity)  
	[1, 2, 3]  

	flatMap()方法对原数组的每个成员执行一个函数，相当于执行Array.prototype.map(),然后对返回值组成的数组执行flat()方法。该方法返回一个新数组，不改变原数组。 flatMap()只能展开一层数组。  
	[2, 3, 4].flatMap((x) => [x, x * 2]) // 相当于 [[2, 4], [3, 6], [4, 8]].flat()  
	[2, 4, 3, 6, 4, 8]
	
4. 数组和对象有哪些常用的原生方法。  
     Array.toString( )          Object.toString( )  
	Array.length 数组的大小            Object.hasOwnProperty( ) 检查属性是否被继承  
	Array.push( ) 给数组添加元素  
	Array.sort( ) 对数组元素进行排序  
	Array.splice( ) 插入、删除或替换数组的元素  
	Array.pop( ) 删除并返回数组的最后一个元素  
	Array.join( ) 将数组元素连接起来以构建一个字符串  
	Array.shift( ) 将元素移出数组  
	Array.reverse( ) 颠倒数组中元素的顺序  


5. Class
  
	
6. 