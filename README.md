




# Horiken_2020_0

事前情報ありの環境において，ゴールを目指しながら各経由地を巡回し，予め指定した交差点・探索エリアで必要なノードを起動，それらの状況に対応する行動させるプログラムです．


 
# DEMO
自律移動中の信号認識
https://user-images.githubusercontent.com/73274492/109469232-1da3b480-7ab1-11eb-8515-1dd8ba2152a4.mp4

自律移動中の物体探索
https://user-images.githubusercontent.com/73274492/109469242-20060e80-7ab1-11eb-9342-072aad7e1ee3.mp4

<img width="271" alt="2021-03-01 (1)" src="https://user-images.githubusercontent.com/73274492/109474570-00beaf80-7ab8-11eb-995d-d6e1e00171c0.png">
<img width="144" alt="2021-03-01 (2)" src="https://user-images.githubusercontent.com/73274492/109474574-02887300-7ab8-11eb-820b-6df040fac9be.png">





# Features
自律移動の途中でその都度必要なノード呼び出しにはactionlibを用いてServer/Clientによる構造を用いて呼び出している．
Serverは常に起動させておき，smachでactionlibを用いた特定の位置指定をしたエリアにClientを配置することでノードを途中起動させています．


交差点では事前に指定したWPによって交差点領域内に入る前に一時停止，信号認識ノード起動→信号機が赤の間は停止し，青になったら自律移動再開．

探索エリアでは事前に指定したポイントで探索ノード起動→探索対象が見つかるまで何度か探索し，発見したら探索対象に0.5mまで接近し，検知完了とし本来のゴールを目指す（制限時間と再試行回数設定 ：制限時間内では見つけるまで車体回転し続け，それを設定回数分だけ繰り返し，検知できたら次の行動へ移る．検知できなくても探索を諦め次の行動へ移る）．
# Requirement
 
動かすのに必要なライブラリなどを列挙
 
(ros-melodic)

boundingbox_msgs

darknet_ros

navigation

slam_gmapping

openni_camera

gazebo_ros_demos

robot_arm_ros/diff_drive

executive_smach

executive_smach_visualization


 
# Installation
 
Requirementで列挙したライブラリなどのインストール方法を説明する
 
```bash
sudo apt-get install ros-melodic-navigation
sudo apt-get install ros-melodic-slam-gmapping
git clone --recursive https://github.com/leggedrobotics/darknet_ros.git
git clone https://github.com/ros-simulation/gazebo_ros_demos.git
git clone https://github.com/parambeernegi/robot_arm_ros
git clone https://github.com/ros-drivers/openni_camera.git
git clone https://github.com/ros/executive_smach.git
git clone https://github.com/ros-visualization/executive_smach_visualization.git
```
 
# Usage
 
DEMOの実行方法など、"Horiken_2020_0"の基本的な使い方を説明する
 
```bash
git clone https://github.com/ken-hori-2/Horiken_2020_0.git
cd catkin_ws
catkin build
roslaunch mighty_rover diff_drive.launch
roslaunch ros_beginner mighty.launch
rosrun depth_estimater test.py
rosrun ros_beginner AAA_test.py
rosrun smach_viewer smach_viewer.py
```
 
# Note
 AAA_test.pyを実行すると動き始めてしまうのでまとめられるもの以外は一つにまとめずに別々で起動させてます．
# Author

* 作成者 ken
* 所属 Klab
* E-mail
 
# License
