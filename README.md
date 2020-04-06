# 四轮小车底盘模型
由Solidworks建模利用插件导出模型<br>

#### Todo
* 用xacro改写小车模型,现在主流的建模都是xacro
#### 功能更新
* 向turtle1/cmd_vel话题发布速度信息，小车可以运动(可以直接用turtlesim里面的键盘控制)
* 在gazebo和rviz显示雷达数据
#### 一些说明
* Solidworks生成的只是模型，没有运动控制插件
* 小车的代码主要更新在**smart_car.urdf**文件里，直接运行这个launch文件就可以看到效果
,配置的同时打开gazebo和rviz环境
* 刚开始小车的运动是反的,给的指令往前，小车朝后，给的指令右转，小车左转<br>
ans:后来更改了轮子在joint里面的旋转方向就解决这个问题了(修改向右旋转90°)