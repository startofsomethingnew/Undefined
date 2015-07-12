#编码规范

**良好的编码规范**，

 - 使得代码风格一致，让阅读者专注于内容而不是布局。 
 - 使得阅读者能凭借一致风格，更快地理解代码。 
 - 使得代码便于复制，更改和维护。 
 - 使得体现出的编码的最佳体验。

 > —— [MSDN: C# Coding Conventions](http://msdn.microsoft.com/en-us/library/ff926074.aspx)

---

**关于本文**：

 - **[文件版本](http://en.wikipedia.org/wiki/Software_versioning)**：Alpha 0.0.6；
 - **最后修改时间**：2015.07.11；

---
## 目录

> **1.** [代码风格](RobitCppCodingConventions.md#1-代码风格)
> > **1.1.** [命名举例](RobitCppCodingConventions.md#11-命名举例)<br>
> > **1.2.** [变量命名](RobitCppCodingConventions.md#12-变量命名)<br>
> > **1.3.** [常量命名](RobitCppCodingConventions.md#13-常量命名)<br>
> > **1.4.** [方法命名](RobitCppCodingConventions.md#14-方法函数命名)<br>
> > **1.5.** [注释风格](RobitCppCodingConventions.md#15-注释风格)<br>
> > **1.6.** [排版](RobitCppCodingConventions.md#16-排版)

> **2.** [代码规范](RobitCppCodingConventions.md#2-代码规范)<br>
> > **2.1.** [头文件](RobitCppCodingConventions.md#21-头文件)<br>
> > **2.2.** [类](RobitCppCodingConventions.md#22-类)<br>
> > **2.3.** [常量](RobitCppCodingConventions.md#23-常量)<br>
> > **2.4.** [变量](RobitCppCodingConventions.md#24-变量)<br>
> > **2.5.** [其它未分类部分](RobitCppCodingConventions.md#25-其它未分类部分)<br>

> **3.** [开发工具相关](RobitCppCodingConventions.md#3-开发工具相关)
> > **3.1.** [推荐开发工具](RobitCppCodingConventions.md#31-推荐开发工具)<br>
> > **3.2.** [Microsoft Visual Studio (2013)](RobitCppCodingConventions.md#32-microsoft-visual-studio-2013)

> **0.** [附录](RobitCppCodingConventions.md#0-附录)

---
##  **1. 代码风格**

### 1.1. 命名举例

在较为详细的介绍之前，使用这个例子，给大家一个直观的印象

以student name举例：

| 类型 | 风格 | 举例 |
| --- | --- | --- |
| 类、结构 | Pascal | StudentName
| 方法、函数 | camel | studentName
| 方法参数 | camel | studentName
| 局部变量 | camel | studentName
| 私有成员变量 |  | _StudentName
| 常量 |  | STUDENT_NAME
| 枚举类型 | Pascal | StudentName
| 枚举类型值 |  | STUDENT_NAME


 > **注**：
 > 
 >	- **camel命名法**：从第二个单词开始单词首字母大写，如：studentName。
 >	- **Pascal命名法**：所有单词首字母大写，如：StudentName。
 - **部分参考**：[.NET名称准则](http://msdn.microsoft.com/zh-cn/library/ms229002(v=vs.100).aspx)

推荐参考附件，能获得更好的体验；

### 1.2. 变量命名
**原则**：命名应该尽可能直观，能够通过名称来体现其*类型*和*用途*。

**命名风格**：

 - **方法参数**、
 - **局部变量**：使用`camel`命名法；
 - **成员变量**：使用`_`前缀，以及`Pascal`命名法；

> **注**：[关于匈牙利命名法的一些讨论](http://blog.csdn.net/fullsail/article/details/8039253)。

**注意事项**：

 - 避免使用会出现歧义的英文缩写；
 - 禁止使用拼音作为变量名称，如bitren；
 - 只有*作用域非常小*的循环中才允许使用i、j、k等命名的*循环控制变量*；

### 1.3. 常量命名
**原则**：简洁，体现其*分类*和*用途*。
**格式**：*大写*，单词之间使用*下划线*连接。

 > **e.g.** 
 
	const int TERRAIN_WIDTH = 16000;
	const int TERRAIN_HEIGHT = 9000;

**注意事项**：

 - 注意区分使用枚举类型和常量的场合；


### 1.4. 方法(函数)命名

**格式**：使用`camel`命名法；

**注意事项**：尽可能使用动词作为方法名的第一个词；

### 1.5. 注释风格

**原则**：尽量**简明扼要**。

**类型**：

- 文件注释：文件最顶端，标明文件用途，文件版本，修改日期，修改人等；
- 函数注释：标明*函数用途*，输入*参数*意义，*返回值*意义和*异常*信息（如果有的话）；
- 变量注释：常量、类的成员变量等都需要加上，标明*变量用途*；
- 其它：函数内部的注释使用`/* 内容 */`，在相应语句上方紧靠；

**注释语言**：中文

 > **注：**
 > 
 > - 各IDE的字符编码设置不统一，使用中文时统一使用`UTF-8`编码；

**风格**：[Doxygen](http://www.doxygen.nl/)；

 - **文件注释**：
	
		/**********************************************************************
		 *
		 *	@file		file.h
		 *	@brief		Introduction.
		 *
		 *	Date        Name        Description
		 *	dd/mm/yy	Author		Creation.
		 *
		 *********************************************************************/

 - **函数注释**：

		/**
		 *	\brief 方法: 取最大值
		 *
		 *	\param	numA		比较整数值numA
		 *	\param	numB		比较整数值numB
		 *
		 *	\return 			numA和numB中大的那一个	
		 */
		int Max(const int numA, const int numB);

 - **成员变量的注释**：
 
		int _Height;										/**< 场地 高度 */


**注**：头文件应该拥有非常详细、规范的注释。相比之下`.cpp`文件要求则不这么高。

### 1.6. 排版

**原则**：保持统一的全局风格，尽可能提高代码可读性。

**空格**：

 - 关键词和操作符之间加适当的空格；
 - 每个`,`之后添加一个空格；

**换行**：

 - 避免一行超过**78**个字符；
 - 较长的语句、表达式等要分成多行书写；

 > **e.g.** 

		if (a == b 
		    && b == c
		    && c == d
		    && d == e) {
		    /* 内容 */
		}

 - 若函数或过程中的参数较长，则要进行适当的划分；
 - 划分出的新行要进行适应的缩进，使排版整齐，语句可读；

**空行**：

 - 相对独立的程序块与块之间加空行；

**“{”，“}”**：

 - 函数实现部分的大括号，各自应该单独占用一行；
 > **e.g.** 

	    int Point::
		getX() const
		{
		    /* 内容 */
		}
 
 - if \ while \ for \ switch 等语句，保持 {} 最少占用行数的风格；
 
 > **e.g.** 

		if ( true ) {
		    /* 内容 */
		} else {
		    /* 内容 */
		}

 - lambda表达式，只有在表达式很短的场合下保持`{}`在同一行；

**“/*  */”**：

 - 适用于描述性的注释；

**“//”**：

 - `TODO:`标签(详细说明请参见本文3.2.)；
 - 暂时需要删除的代码；
 
  > **注**： 如果某段代码已经确定废弃，请及时删除它，而不是以 `//`的形式保留下来 
 
 - **约定**：一定要从功能上区分开`// 待修改的部分`与`/* 描述的部分 */`。
 - **重要**：使用这风格的注释请加上注释人的英文名称；

**部分参考**：[编码规则](http://baike.baidu.com/view/11771102.htm?fr=aladdin)。

---
## **2. 代码规范**

### 2.1. 头文件

**文件路径**：由头文件的*用途*和*作用范围*决定

**"include"顺序**：标准C头文件、标准C++头文件、系统头文件、自定义头文件；

**防止多重包含**：最顶端使用`#pragma once`

**内容**：只能包含以下部分：

 - 注释；
 - 预处理语句 (#include \\ #define \\ #ifdef...)；
 - 类、结构的*声明*等；

 > **注**：
 > 
 > - 声明：只给出原形，例如对于函数来说即返回值，参数和函数名；
 > - 定义：给出具体代码；

**注意事项**：

 - 头文件应该尽量少的包含其它头文件；


### 2.2. 类


**访问控制**：

 - 类中推荐声明的顺序是：public、protected、private；
 - 禁止使用公有成员变量，尽可能使数据隐藏。
 - 私有成员一般使用 setter 和 getter 方法来修改和获取；
 
**构造、析构函数**：

 - 构造函数不能为虚函数，而析构函数可以且常常是虚函数；
 - 保证每个对象都在构造函数有初始化；
 - 请使用初始化成员列表(Member Initialization List)替代构造函数内的赋值；
 - 初始化成员列表的初始化顺序应该和class中声明的次序相同；
 - 含有指针成员的类，请保证重载拷贝构造函数(Copy Constructor)；
 - 在构造函数、析构函数不要调用虚函数；
 
**操作符重载**：

 - 含有指针成员的类，请保证重载赋值运算符`=`；
 - 重载+=、=、-=这类运算时，请确保`return *this`的引用；
 - 重载+、-这类二元运算符，请使用友元`friend`，并返回一个`const`的临时对象；

**类的方法**：

 - 避免在同一个类的两个代码块中出现完全相同的代码；
 - 避免很长的方法，如果这个方法已经达到几百行，请重新组织代码并拆分它；

**其它**：

 - 一个类应该保持单一功能，否则请考虑拆分它；
 - 一般不要对类中的`public`部分添删；
 - 避免使用大类，如果这个类已经达到几千行，请重新组织代码并拆分它；

**附**：

 - 部分参考：[C++类和接口的设计原则探讨](http://www.warting.com/program/201208/53517.html)、[C++ 类的设计规则](http://blog.csdn.net/heliang1108/article/details/8825233)。
 - 推荐大家了解一些设计模式：[百度百科：设计模式](http://baike.baidu.com/view/66964.htm?fr=aladdin)、[Wikipedia: Software design pattern](http://en.wikipedia.org/wiki/Software_design_pattern)。

### 2.3. 常量

**要求**：

- 使用`const`常量，而不是宏定义常量`#define`；

	> **注**：[关于C++ const全面的总结](http://blog.csdn.net/Eric_Jo/article/details/4138548)
	> **推荐阅读**： Effective C++ 3td, item 3.

- 任何可能会修改的、可能多次出现的*数字*或*字符串*等类型都须定义为常量；
- 如果某一常量与其它常量密切相关，应给出相应的关系； 

 > **e.g.** 

		const int DATA_MAX = 10000;
		const int DATA_MIN = 0;
		const int DATA_MID = (DATA_MAX + DATA_MIN) / 2;

- 单个类使用的常量应该进行*封装*，确保外部无法访问；

	> **e.g.** 某个运球方案中的移动距离、移动角度。 

- 多个文件都使用的常量可以放入一个公共的头文件中；

### 2.4. 变量

**全局变量**：禁止使用全局变量；

**局部变量**：满足以下要求：

 - 确保变量在其最小作用域；
 
 > **e.g.** 使用 `for(int i = 0; i < n; i++)`而不是 `int i; … for(i = 0; i < n; i++)`。

 - 局部代码块中临时变量以一两个为宜，如果超过三个就应该考虑重新组织。

**注意事项**：

 - 每一个`new`都必须要有对应的`delete`，避免出现内存泄漏；
 - 操作指针时**必须**确保它不是`nullptr`；
 - 禁止操作未初始化的变量，推荐在声明的同时初始化；
 - 使用C++风格的类型转换而不是C风格的类型转换；

### 2.5. 其它未分类部分

**文件编码**：

 - 保持所有文件为 `UTF-8` 编码；

**STL等其它库，注意事项**：

 - 命名空间：一个文件最多使用一个命名空间，同时不要使用命名空间`std`；

 > **注**：
 > 对于stl中的cout，使用`std::cout`，
 > 而不是`using namespace std`、`cout`或者`using std::cout`。

 - 禁止使用库中不稳定的功能；

**关于一些C++新特性**：

 - 对非基本类型，推荐灵活使用C++11中`auto`关键字(自动类型推断)；

 > **e.g.**
 > 推荐使用：

		for (auto &it : list) 
		    delete it;

 > 而不是： 
 
		 for (std::list<TYPE*>::iterator it = list.begin(); it != list.end(); it++) 
		     delete *it;


---
## **3. 开发工具相关**

### 3.1. 推荐开发工具

 - 待补充

### 3.2. Microsoft Visual Studio (2013)

**常用快捷键**：

 - 查找：Ctrl + F
 - 查找和替换：Ctrl + Shift + F
 - 替换：Ctrl + H

 > 相比Ctrl + F有更高级的选项

 - 代码整理：Ctrl + K, Ctrl + F

 > 只作用于选中部分，推荐结合Ctrl + A(全选)使用

 - 复制：Ctrl + C
 
 > 如果未选取复制内容，将默认复制光标那一整行

 - 注释：Ctrl + K, Ctrl + C
 - 取消注释：Ctrl + K, Ctrl + U
 
  > 只按下 Ctrl + U 是转换为小写，Ctrl + Shift + U 为转换大写

 - 头文件、源文件之间切换：Ctrl + K, Ctrl + O

 - 向上（下）移动整行代码：Alt + ↑(↓)
 - 查看定义、声明：Alt + F12

**使用TODO标记**：

TODO标记用于标记一些之后才完成的事。

 - 创建：在要标记的地方输入：`// TODO: 具体内容`
 - 查看：视图 - > 任务列表 - > 注释

**约定**：

 - 标记为自己将要完成的事，使用`// TODO[标记者英文名称缩写]: 具体内容`
 - 希望别人完成这个地方，`[]`中不写名称即可

---

### 0. 附录

**其它参考文章**：

 - [代码规范那些事](http://blog.csdn.net/kimylrong/article/details/7700311)；
 - [Qt编码规范](http://blog.csdn.net/dbzhang800/article/details/6381636)；
 - [一些VS2013的使用技巧](http://www.cnblogs.com/h46incon/p/3578735.html)；


**相关信息**：

 - 推荐的在线MarkDown编辑、阅读工具：[stackedit](https://stackedit.io/)
 - 本文[MarkDown](http://en.wikipedia.org/wiki/Markdown)语法参考：[Markdown 语法说明](http://wowubuntu.com/markdown/#em)
