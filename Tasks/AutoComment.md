正确的偷懒姿势，其一
---

**Date**: 2015.07.15
**Author**: MYLS
**Principal**: MYLS

####限制条件：

 - **难度**：2
 - **限定语言**：N/A
 - **人数限制**：1
 - **依赖任务**：N/A

####任务描述：

 - **简介**：每次任务都要求那么多重复、死板、虽然看起来很厉害但是好像没什么用的注释？其实我也很烦……所以如何找一个平衡的偷懒姿势…？试着写一个为`.h`、`.hpp`文件**自动添加注释**的程序吧！虽然它不能帮你写出`\brief`等等的介绍内容，但是还是能帮你省去了复制粘贴注释格式的时间。
 - **需求**：
    1. 程序通过简单方式就能找到待补全注释的文件的路径，而不是路径固定在程序内，每次都要重新编译。
    2. 需要增加的注释，参考：[RobitCppCodingConventions](ref/RobitCppCodingConventions.md#15-注释风格)
    3. 补全能补全的部分，比如函数、方法注释中，`\param`的参数名称等等
    4. 你有可能需要考虑各种细节，比如是否备份原文件，是否已经存在注释……

 - **关键词**：`Doxygen`, 文件读写, `lexical analysis`
 - **参考资料**：
