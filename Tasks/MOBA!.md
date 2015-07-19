"What does a hero truly need?"
---

**Date**: 2015.07.11
**Author**: MYLS
**Principal**: LZ

####限制条件：

 - **难度**：N/A
 - **限定语言**：C++
 - **人数限制**：1
 - **依赖任务**：N/A

####任务描述：

 - **简介**：
    - 介绍：

	> Often I am asked, what does a hero truly need?<br>
	> Much depends on the hero.<br>
	> would you be **swift**? There for you I have speed beyond measure!<br>
	> Would you be **strong**? Then I can grant you the might to overpower any foe.<br>
	> Would you be **wise**? Then come closer and I will unlock your inner cunning.<br>
	> What does a Hero truly need?<br>
	> That is for you to decide.<br>

    - 某 MOBA 游戏有这样一个设定，英雄们分为三类，*敏捷*型、*力量*型、*智力*型
    - 这是因为英雄都有三个可成长的属性，分别为：*敏捷*、*力量*、*智力*，属性值满足线性关系：属性值 = 属性成长值 * (等级 - 1) + 基础属性。
    - 但是英雄的类型直接影响了他们的攻击力，其计算方式为 攻击力 = 主属性值 + 基础攻击力。(例如，敏捷型英雄主属性为敏捷，以此类推)
    - 那么问题来了，TB想要知道自己到达25级的时候，自己的各项属性。

 - **需求**：
    1. 我们需要抽象基类，`Hero`，包含三种子类类型`StrengthHero`、`AgileHero`、`IntellectualHero`。他们的主属性分别为 Strength 、 Agile 、 Intellectual 。
    2. 对于属性的约定，基础属性为整数，属性成长值为实数，精确到小数点后两位。
    3. 各个固定的数据在构造的时候传入（比如基础属性，属性成长值）。
    4. 拥有一个设定等级的抽象方法。
    5. 可以对子类调 `int getProperty(PropertyType type) const`，获取指定的属性：
    	- 这是一个来自基类的*虚函数*或者*纯虚函数*
    	- 返回值用`int`(*舍*去小数部分)表示
    	- 其中`PropertyType`是一个由你实现的枚举类型，标识三种属性类型以及攻击力
    	- 使用多态相关知识完成它，具体细节由你决定
	6. TB 为*敏捷*类型英雄，他的的属性资料是：

		TB | 力量 | 敏捷 | 智力| 攻击力
		---|---|---|---|---
		基础属性| 15 | 22 | 19 | 29
		属性成长| 1.9 | 3.2 | 1.75 | 0

	那么问题来了，TB 达任意等级（比如25级）的时候，各个属性是…？
	7. 符合*代码规范*：[RobitCppCodingConventions](ref/RobitCppCodingConventions.md)


 - **关键词**：Inherit, Polymorphic, override, `(Pure) virtual function`
 - **参考资料**：
 	- [Effective c++学习笔记——条款07:为多态基类声明virtual析构函数](http://blog.csdn.net/wallwind/article/details/6762174)
 	- [[C++]接口继承与实现继承](http://blog.csdn.net/ljinddlj/article/details/1922189)
 	- [C++ 设计抽象基类的策略](http://blog.csdn.net/slience_perseverance/article/details/20546955)
 	- [C++封装、继承、多态](http://blog.csdn.net/ruyue_ruyue/article/details/8211809)