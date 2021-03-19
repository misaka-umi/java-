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
* 必须定义在类型内的，为Method方法；可以脱离的是function方法

**member level**（成员级），声明在类型内部
* public，公共，全局可访问
* package-private，包内可访问
* private，私有，类型内访问
* protected，包中及任意位置的子类可访问
//级别仅说明可访问范围，与操作无关
