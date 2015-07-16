堆 x C
---

**Date**: 2015.07.13
**Author**: MYLS
**Principal**: MYLS

####限制条件：

 - **难度**：N/A
 - **限定语言**：C
 - **人数限制**：[1, 2]
 - **依赖任务**：N/A

####任务描述：

 - **简介**：堆系列，其一
这是一个关于数据结构——堆的一些事儿（特指"二叉堆"）。它是一个很常见的数据结构，stl的优先队列就是用它实现的，还有就是，或许你们之前做过一个题可以和这个有关，叫做“合并果子”？。它的具体细节不赘述了。这次我们来实现一下C版本的堆。还记得你的 C 知识么？

 - **需求**：
    1. 实现一个`C`版本的堆，`struct Heap`
    2. 使用 `.c`文件 作为它们的源文件。注意，只能使用C语言的语法！
    3. 在理想情况下你的堆应该支持**任意多**的数据
    4. 请加入必要的**注释**
    5. 或许你不知道该怎么写头文件，所以这里给它。将由你实现它的`.c`源文件：
```
/**********************************************************************
 *
 *	@file		Heap.h
 *	@brief		一个 C 风格的二叉堆
 *
 *	Date        Name        Description
 *	07/13/14	MYLS		Creation.
 *
 *********************************************************************/

#pragma once

// Unix C 命名风格，参考：http://www.linuxidc.com/Linux/2012-01/52293.htm

#ifdef __cplusplus
extern "C"
{
#endif

	typedef int Heap_element;
	/**
	 *	\brief	二叉堆，C 版本
	 */
	typedef struct Heap {
		Heap_element * array;		/**< 存储元素的数组 */
		int is_min_heap;			/**< 是否是最小堆 */
		
		// TODO: 补全你需要的其它数据成员
	} Heap;

	/**
	 *	\brief	构造一个 空堆
	 *
	 *	\param	heap		待初始化的堆
	 *	\param	is_min_heap	0为小根堆，其它情况下为大根堆
	 */
	void create_heap(Heap * heap, int is_min_heap);

	/**
	 *	\brief	删除一个已经构造的堆
	 *
	 *	\param	heap		待删除的堆
	 */
	void delete_heap(Heap * heap);

	/**
	 *	\brief	复制一个堆
	 *
	 *	\param	src			复制的来源
	 *	\param	dest		复制的目标
	 */
	void copy_heap(Heap * src, Heap * dest);

	/**
	 *	\brief	弹出堆顶元素
	 *
	 *	\param	heap		被操作的堆
	 */
	void pop_heap(Heap * heap);

	/**
	 *	\brief	压入一个元素
	 *
	 *	\param	heap		被操作的堆
	 *	\param	element		被压入的元素
	 */
	void push_heap(Heap * heap, Heap_element element);

	/**
	 *	\brief	检查堆是否问空
	 *
	 *	\param	heap		被操作的堆
	 *
	 *	\return				0 为空; 1 非空
	 */
	int is_empty(Heap * heap);

	/**
	 *	\brief	获取栈顶元素
	 *
	 *	\param	heap		被操作的堆
	 *
	 *	\return				栈顶元素
	 */
	Heap_element get_top(Heap * heap);

#ifdef __cplusplus
}
#endif
```
 - **关键词**：`Binary Heap`, Process-Oriented, `realloc`, `malloc`, `free`
 - **参考资料**：[wiki: Binary heap](https://en.wikipedia.org/wiki/Binary_heap)
