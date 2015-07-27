直方图与鼠标事件
---

**Date**: 2015.07.27
**Author**: TB
**Principal**: TB

####限制条件：

 - **难度**：N/A
 - **限定语言**：C/C++
 - **人数限制**：1
 - **依赖任务**：[ColorModel](ColorModel.md)

####任务描述：

 - **简介**：先用刚学到的东西实现一个使用的获取图像某块区域各通道直方图的程序吧！
 - **需求**：
    1. 用 OpenCV 相关函数载入并显示一张彩色图像并将其用`cvSplit`分为三个通道的图像
    2. 调用 OpenCV 鼠标事件实现在图像上圈出一个方框（其他形状均可）
    3. 使用相关方法或自己编写方法统计获得此区域在各通道的直方图

 - **关键词**：`Histogram`, `Mouse events`, `cvRectangle`, `cvCircle`, `cvSetImageROI`
 - **参考资料**：
 	- [学习OpenCV——鼠标事件（画框)](http://m.blog.csdn.net/blog/kaka20080622/44087711)
 	- 书籍：学习OpenCV::第七章::直方图与匹配