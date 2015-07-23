一起来做动画吧！
---

**Date**: 2015.07.23
**Author**: HAQ
**Principal**: HAQ

####限制条件：

 - **难度**：N/A
 - **限定语言**：C++
 - **人数限制**：1
 - **依赖任务**：[ColorfulBubbles](ColorfulBubbles.md)

####任务描述：

 - **简介**：有了前三次QT作业的基础，大家想必对QT绘制界面都有了一定的了解吧？这次来做个有趣的东西，我们来做动画~
旧时动画片都是通过一张一张图片以一定的速度按顺序展示，形成一种动态的效果的。那么今天我们来体验一下这项的技术，做一个小动画。
 - **需求**：
	1. 去除主窗体标题栏
	2. 界面正中央一显示动画的矩形，启动界面时动画定格在第一帧的画面
	3. 画面下方有三个按钮，start，stop，close，作用分别是画面动起来，让动画定格，关闭程序
	4. 动画要求在40帧以上
	5. 提示：
		1. 动画内容无要求，大家可以自己用播放器进行截图
		2. 可以用`QLabel`或`QGraphicsScene`或其他你认为可行的方式来完成

 - **关键词**：`QTimer`, `QLabel`, `QGraphicsScene`, `QPainter`
 - **参考资料**：[Qt5 Tutorial QGraphicsView and QGraphicsScene](http://www.bogotobogo.com/Qt/Qt5_QGraphicsView_QGraphicsScene.php)
