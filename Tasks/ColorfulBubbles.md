七彩的泡泡
------------

**Date**: 2015.07.19 
**Author**: HAQ 
**Principal**: HAQ

####限制条件：

 - **难度**：N/A
 - **限定语言**：C++ 
 - **人数限制**：1
 - **依赖任务**：N/A

####任务描述：

 - **简介**：QT第一课！大家都见过满屏晃动的泡泡的屏保吧，我们现在就来做一个它基本的雏形吧，在主窗体上绘制一幅七彩泡泡的画面。
 
 - **需求**：
	1. 要求泡泡的数量大于20个，位置随机
	2. 泡泡的大小不一，在一定范围内
	3. 泡泡的要有颜色，为了美观，其中必须出现一些渐变色的泡泡，并且每个泡泡都具有一定的透明度
	4. 提示：可以通过重写`QMainWindow`的成员函数`paintEvent`来实现
	5. 符合*代码规范*：[RobitCppCodingConventions](ref/RobitCppCodingConventions.md)

 - **关键词**：`QPainter`、`QPaintEvent`、`QPen`、`QBrush`、`qrand()`
 - **参考资料**：[RGB颜色对照表](http://tool.oschina.net/commons?type=3)

 