七彩的图形
------------

**Date**: 2015.07.20
**Author**: MYLS
**Principal**: MYLS

####限制条件：

 - **难度**：N/A
 - **限定语言**：C++ 
 - **人数限制**：1
 - **依赖任务**：[ColorfulBubbles](ColorfulBubbles.md)

####任务描述：

 - **简介**：QT 第二课。多态、继承又回来了！会动的，带淡入淡出的，多种图形……
 
 - **需求**：
	1. 需求变更。除了泡泡，还需要随机的*三角形*、*正方形*、*五角星*各10个！他们都是基类`Shape`的*派生类*
	2. 所有的形状，*大小*、*颜色*随机，同时设定为*渐变色*。*透明度*由 0~255~0 周期变化。其它细节自定。
	3. `Shape`拥有：
		- `virtul void update() const = 0`，更新对象数据。在*窗口*范围内平移（遇到边界则镜面反弹），更新透明度数据等事项
		- `virtul void draw() const = 0`，绘制这个对象
	4. 符合*代码规范*：[RobitCppCodingConventions](ref/RobitCppCodingConventions.md)

 - **关键词**：`QTimer`、`QPainter`、`QPaintEvent`、`QPen`、`QBrush`、`qrand`、`QLabel`
 - **参考资料**：

 