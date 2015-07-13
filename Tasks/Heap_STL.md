堆 x STL
---

**Date**: 2015.07.14
**Author**: MYLS
**Principal**: MYLS

####限制条件：

 - **难度**：1
 - **限定语言**：C++
 - **人数限制**：1
 - **依赖任务**：[Heap_Cpp](Heap_Cpp.md), [Timer](Timer.md)

####任务描述：

 - **简介**：堆系列，其三
哈，我猜你一定想知道你写的C语言版本的堆和C++版本的堆，谁的效率更高？一起来试试吧。不过我们还得多带一个来自STL的小伙伴——优先队列！（虽然名字不一样，脱掉马甲大家都是堆）

 - **需求**：
    1. 仍然使用上一个任务，C++版本的堆的所在工程
    2. 查找STL容器：`std::priority_queue`相关资料，熟悉并试着使用它
    3. 做一个包含前两次中，C语言的堆、自己写的C++版本的堆，以及`std::priority_queue`，三个堆的测试例子
    4. 借助你的Timer，测试并统计一下，三个堆处理相同数据量，各自的操作花费的时间
    5. 虽然没有多少代码，但是还是须要符合*代码规范*：[RobitCppCodingConventions](ref/RobitCppCodingConventions.md)

 - **关键词**：`Binary Heap`, `Debug`, `Realse`
 - **参考资料**：[std::priority_queue](http://www.cplusplus.com/reference/queue/priority_queue/)
