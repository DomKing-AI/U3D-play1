#### 介绍
基于Qt的2048小游戏的设计与开发

#### 项目描述

1. 创建一个基于Qt的应用程序，包括主窗口、游戏面板和控制按钮。
2. 设计一个4x4的游戏面板，用于显示数字方块。
3. 实现游戏逻辑，包括随机生成数字方块、移动方块、合并方块以及判断游戏是否结束。
4. 添加控制按钮，如“上”、“下”、“左”、“右”等，用于控制方块的移动方向。
5.添加删除功能，如通过鼠标（左/右键）双击数字方块，清除所点击的数值。
6.添加重新开始控制按钮，实现对游戏的重置功能。
7.添加动画特效，如通过设置动画开始时和结束时的坐标和大小，实现方块的缩放动画。
8. 优化界面和用户体验，使其易于操作和理解。
9. 添加游戏得分功能，记录玩家在游戏中获得的分数。
10.添加游戏最高得分功能，记录玩家在多次游戏中的的最高分数。
11. 提供游戏教程和帮助信息，帮助玩家更好地了解游戏规则和操作方法。
12. 将项目打包成一个可执行文件，方便用户安装和使用。

#### 开发环境

硬件平台 64 位Intel x86及兼容处理器个人计算机
操作系统 Ubuntu 16.04 LTS 32
开发工具 g++ version 5.4.0、Qt Creator 3.5.1  based on Qt 5.5.1、MySQL数据库

#### 基础功能

1. 游戏面板：显示一个4x4的数字方块，每个方块上的数字表示其数值。
2. 随机生成数字方块：在游戏开始时，随机生成两个数字方块，它们的初始值为2或4。
3.动画特效：每当有新的数字方块生成时，该生成的方块就会播放一次由小到大的缩放动画。
4. 移动方块：玩家可以使用方向键（上、下、左、右）来控制方块的移动。当玩家按下方向键时，所有相邻且相同的数字方块会向该方向合并。
5.删除方块：玩家可以使用鼠标（左/右键）双击来删除方块的数值。
6. 合并方块：当两个相邻且相同的数字方块相遇时，它们会合并成一个更大的数字方块，新的数字方块的值等于原来两个数字方块的值之和。合并后，原来的数字方块会变成空白方块。
7. 判断游戏结束：当游戏面板中没有空白方块，且无法通过移动方块来合并数字方块时，游戏结束。此时，程序会弹出一个提示框(QMessageBox)，让玩家选择是否结束或重开一局。
8. 计分功能：
(1).记录玩家在游戏中获得的分数，每合并一个数字方块，分数加数字方块中的数字。
(2).记录玩家在游戏中的最高分数，每当超过最高分数时，最高分数将被刷新。
9. 教程和帮助信息：提供游戏教程和帮助信息，帮助玩家更好地了解游戏规则和操作方法。

#### 所用技术

1. Qt框架：使用Qt框架进行开发，它是一个跨平台的应用程序开发框架，提供了丰富的图	形界面组件和事件处理机制。
2. 面向对象编程（OOP）：使用面向对象的编程方式，将游戏的逻辑和界面分离，使得代码更加模块化和易于维护。
3. 信号与槽机制：Qt框架中提供了信号与槽机制，用于实现对象之间的通信。在游戏逻辑中，可以使用信号与槽机制来响应用户的操作，如按下方向键、移动方块等。
4. 二维数组：使用二维数组来表示游戏面板，每个元素代表一个数字方块。通过操作二维数组，可以实现对游戏面板的访问和修改。
5. 随机数生成：使用随机数生成函数，如rand()或qrand()，来生成随机的数字方块。
6. 事件处理：使用Qt的事件处理机制，如mousePressEvent()、keyPressEvent()等，来响应用户的输入操作。
7.动画处理：使用Qt控件的动画，如QPropertyAnimation、setStartValue(QRect(x,y,w,h))、
setEndValue(QRect(x,y,w,h))等，通过控制控件的初始和结束的位置及大小来实现动画特效。
8. 图形界面设计：使用Qt的图形界面设计工具，如Qt Designer(Qt设计师)，来设计和布局游戏界面。

#### 模块划分

主要分为游戏面板模块、随机生成数字方块模块、移动方块模块、删除方块模块、合并方块	模块、判断游戏结束模块，动画显示模块，计分功能模块、教程和帮助信息模块等。

#### 成品展示

![2048-1](https://github.com/DomKing-AI/Qt-2048/assets/145100218/59912eb4-81aa-4233-b773-26f30fc7808f)
![2048-2](https://github.com/DomKing-AI/Qt-2048/assets/145100218/7282e4b7-1410-47a6-9665-61a565d6c137)

