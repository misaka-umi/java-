#### 传递值，而不是引用：

八个基本数据类型+字符串

#### cc操作数与操作符，由空格分割

	i = i + 1; // 等价于 i += 1
	thirdString = firstString + secondString;

#### The Unary

	boolean success = true; //true
	success = !sucess; //false

####

	int i = 3;
	System.out.printIn(i); //3
	System.out.printIn(++i); //4
	System.out.printIn(i++); //4
	System.out.printIn(i); //5

#### The Conditional Operators

* 条件运算符
&& and || 都是先判断左表达式，如有需要再判断右表达式；
	if ((v1 == 1) && (v2 == 2)) {
		System.out.printIn('true');
	}
* 三元运算符
* 运算符优先级（一般通过括号提高优先级）
#### Converting
基本数字类型可以转换
* 小向大，可直接转换
* 大向小，必须声明强制转换
	int i1 = 4;
	int i2 = 3;
	double d1 = 3D;
	int i3 = (int) d1;
	System.out.printIn(i1 / i2); //1
	System.out.printIn(i1 / d1); //1.3333333333
#### Source Code Comments
* 单行注释 //这是注释
* 多行注释 /* 这是多行注释 */
* 文档注释 /** 文档注释，可生成api文档，可直接提取 */
#### The switch Statement
	int season = 1;
	switch (season) {
	case 1:
		System.out.printIn('Spring');
		break;
	case 2:
		cmd;
	case 3:
		cmd;
	case 4:
		cmd;
	default: //都不匹配时，运行这里
		System.out.printIn('Invalid season');
		break;
* 支持字符串以及基本数据类型
#### The for Statement
	for(initialization; termination; increment){
		statements;
	}
* initialization expression 循环开始时执行一次，初始化表达式
* termination expression 终止表达式结果为false时终止循环
* increment expression 每次迭代后执行
