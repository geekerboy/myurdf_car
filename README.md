# 四轮小车底盘模型
由Solidworks建模利用插件导出模型<br>

#### Todo
* 用xacro改写小车模型,现在主流的建模都是xacro


* 在gazebo和rviz显示雷达数据
#### 一些说明
* Solidworks生成的只是模型，没有运动控制插件
* 代码直接放到本地的一个包里面即可，由于是launch文件不需要catkin_make即可使用
* 小车的代码主要更新在**smart_car.launch**文件里，直接运行这个launch文件就可以打开仿真环境<br>
`roslaunch pkg_name smart_car.launch `<br>
pkg_name为本地包的名称
* 向turtle1/cmd_vel话题发布速度信息，小车可以运动(可以直接用turtlesim里面的键盘控制)<br>
`rosrun turtlesim turtle_teleop_key `<br>
* 默认加载world,在启动的时候可更改world_flag：=false关闭world的加载<br>
`roslaunch pkg_name smart_car.launch world_flag:=false`<br>
* 刚开始小车的运动是反的,给的指令往前，小车朝后，给的指令右转，小车左转<br>
ans:后来更改了轮子在joint里面的旋转方向就解决这个问题了(修改向右旋转90°)<br>
* 默认不启动rviz,在启动的时候可更改rvizr_flag：=true实现rviz的启动<br>
`roslaunch pkg_name smart_car.launch rviz_flag:=true`<br>
rviz_flag和world_flag可以同时设置<br>
`roslaunch pkg_name smart_car.launch rviz_flag:=true world_flag:=false`<br>




