## Classes and Objects
### Design Patterns:Singleton Pattern
* 适合基于贫血模型的设计与开发
* 用于封装数据的类
```
* 用户学生班级订单地址课程等（empty实体类）
* 封装保存数据，不包含任何数据的业务操作（贫血模型）
```
* 用于提供服务的类
```
* 具有主函数的程序入口类，辅助工具类，业务逻辑类，数据持久化类
* 无需保存操作状态，用于操作保存在实体对象中
```
### Access Level Modifiers
* 访问级别修饰，决定可访问范围
* 可见性
```
封装，暴露一部分，不同级别可访问范围不同
暴露api以供操作等
```
**top level**（顶级），独立的源文件，只有类/接口/枚举/注解，支持创建为顶级的独立源文件
* public，所有其他类可访问
* package-private，无修饰符的默认声明，仅包内可访问
```
package com.example09;
import com.example.controllingaccess;
class PackageUser{
	cmd;
} //package级

package com.example09,controllingaccess;
public class PublicUser{
	cmd;
} //public级
//可以在package级里直接找到public级，
//但package级只有在同级包里能看见，子包也不可见
```
* 禁止在一个源码文件中声明两个并列的类型，降低代码可读性
* package级允许文件名与类名不同，但禁止使用
* 必须定义在类型内的，为Method方法(.java)；可以脱离的是function方法

**member level**（成员级），声明在类型内部
* public，公共，全局可访问
* package-private，包内可访问
* private，私有，类型内访问
* protected，包中及任意位置的子类可访问
//级别仅说明可访问范围，与操作无关
### Defining Methods

方法的组成
* 修饰符，public等
* 方法返回类型，若没有返回值则定义void
* 方法名称
* 参数列表
* 方法体
* cc：方法命名规范，动词开始，小驼峰，接形容词名词
```
public double calculate(double Weighted,double average,int point,int level){
	return 0;
} //方法的签名是calculate(double,double,int,int)
//方法签名与修饰符、参数名称都无关
```

### returning a value from a method
* 声明返回类型，在方法中用return返回值
* 声明返回类型与实际的返回类型需匹配
* 若不返回值可使用void，依旧可以使用return语句返回
### overloading methods
* 方法重载，允许有相同名称但参数列表不同。解决了方法功能相同但必须使用不同命名的缺陷
* 基于方法重载，可以设计出抽象灵活的代码
### 封装
* 对操作的封装
```
隐藏功能实现的具体类型，限制对某些操作的直接访问
```
* 对数据的封装
```
隐藏对象的数据类型，限制对数据信息的直接访问
```
* 私有对象类型

### providing constructors for your classes

* 类的构造类型
* 可以通过new操作符，调用构造函数，创建一个类的对象
``` Bicyle bicyle = new Bicyle() ```
* 构造函数不能存在方法签名相同的
* 可通过构造函数创造对象
* 自动为没有显式声明构造函数的类，创一个无参构造函数
* 但是类显式声明了有参的，就不会自动创建
* 声明访问修饰符，通过控制外部调用其构造函数来限制对象创建


