# HAMER_mini v0.1 (Released 28.01.2020)
The HAMER_Mini robot package is designed as a sub-version of the "Halikarnas Modular Educational Robot" main model. ROS Melodic is compatible.

For HAMER main model : https://github.com/Akerdogmus/hamer

Rviz Launching:

    $ roslaunch hamer_mini hamermini_rviz.launch model:=hamer_mini.urdf
    
Gazebo Launching:

    $ roslaunch hamer_mini hamermini_gazebo.launch
    
# HAMER_mini v0.2

ChangeLog v0.2 -- 29.01.2020

--Ultrasonic sensors added.

Requirements:

In order for the sensors to work properly, "gazebo_ros_pkgs" files must be downloaded.

        $ cd ~/hamer_mini/src
        $ git clone https://github.com/ros-simulation/gazebo_ros_pkgs.git -b melodic-devel
        
        
Contributors: Alim Kerem Erdoğmuş
