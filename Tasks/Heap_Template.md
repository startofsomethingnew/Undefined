堆 x Temlpate
---

**Date**: 2015.07.22
**Author**: MYLS
**Principal**: MYLS

####限制条件：

 - **难度**：2
 - **限定语言**：C++
 - **人数限制**：1
 - **依赖任务**：[Heap_Cpp](Heap_Cpp.md)

####任务描述：

 - **简介**：堆系列，其四。朋友，你听说过模板么？你想知道调试STL时看到的各种`template<typename T>`是何方圣神么？模板与泛型编程，让你的类支持多种数据类型，你，值得拥有。PS. 此处不涉及模板元编程。

 - **需求**：
    1. 了解泛型编程以及C++基础语法。
    2. 基于你的`Heap_Cpp`扩充出`template<typename T> class Heap`，并完成这个模板类
    3. 请保证这个模板类应支撑自定义类型，支持自定义类型的比较器
    4. 注意事项：
    	- 使用模板时，声明和实现都需放在头文件中，但是推荐将实现放在*类外部*
    	- 很多操作需要考虑到自定义类型其它类型，`memcopy`等浅拷贝将无法适应深拷贝的场合，注意一些场合应该传递拷贝还是引用
    5. 须要符合*代码规范*：[RobitCppCodingConventions](ref/RobitCppCodingConventions.md)

 - **关键词**：`template`、`Generic Programming`
 - **参考资料**：
 	- [C++模板与泛型编程基础](http://www.cnblogs.com/zhuyf87/archive/2013/03/04/2942208.html)
 	- [C++模板元编程](http://blog.jobbole.com/83461/)
