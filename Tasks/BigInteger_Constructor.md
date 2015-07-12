大整数 系列任务一
---

**Date**: 2015.07.08
**Author**: MYLS
**Principal**: WZD

####限制条件：

 - **难度**：N/A
 - **限定语言**：C++
 - **人数限制**：1
 - **依赖任务**：N/A

####任务描述：

 - **简介**：`BigInteger` 系列任务一！
 ——有时候我们需要大数之间的运算，所以写一个像Java那样的大整数的类吧。
 - **需求**：
    1. 开始写一个`BigInteger`，我们准备三个文件：
        - `BigInteger.h` BigInteger 这个类的声明
        - `BigInteger.cpp` BigInteger 这个类的实现
        - 一个作为程序入口的`.cpp`文件，写一个`main`函数用于测试
    2. 这一次我们仅仅练习一下，无参构造函数，以*数字字符串*为参数的构造函数，拷贝构造函数，析构函数。暂时不考虑加法等运算。
    3. 在`BigInteger.h`的类的声明中，写下这些构造函数们、析构函数：
	```
	   	public:

		/**
		 *	\brief Constructor
		 */
		BigInteger();

		/**
		 *	\brief	The Copy Constructor.
		 *			It is necessary if any pointer member exists.
		 *
		 *	\param	rhs		拷贝对象
		 */
		BigInteger(const BigInteger& rhs);

		/**
		 *	\brief	Constructor[Overloaded], with all of the parameters.
		 *
		 *	\param	string			A string that represents an integer. e.g. "1000"
		 */
		BigInteger(const char string[]);

		/**
		 *	\brief	Destructor
		 */
		~BigInteger();
	```
	4. 这个类需要被设计为可以支持任意长度的数。
    5. 补全构造、析构函数中余下的部分，即`.h`中私有部分，`.cpp`中具体那些构造、析构的具体实现。在构造函数中使用*初始化成员列表*`Member Initializer List`。
    6. 通过 设置断点 调试一下你的构造函数是否成功。
    7. 记住，如果使用了指针的私有成员，那么很可能有必要自己写出拷贝构造函数，重载`=`，(为了效率甚至需要移动构造函数)
    8. 符合*代码规范*：[RobitCppCodingConventions](ref/RobitCppCodingConventions.md)

 - **关键词**：Constructor, Copy Constructor, Destructor, // Move Constructor
 - **参考资料**：
