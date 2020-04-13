# HAMER_mini v0.1 - (Released 28-01-2020)
The HAMER_Mini robot package is designed as a sub-version of the "Halikarnas Modular Educational Robot" main model. ROS Melodic is compatible.

For HAMER main model : https://github.com/Akerdogmus/hamer

Rviz Launching:

    $ roslaunch hamer_mini hamermini_rviz.launch
    
Gazebo Launching:

    $ roslaunch hamer_mini hamermini_gazebo.launch
    
------------------------------------------------------------------------------
# HAMER_mini v0.2

Changelog v0.2 - (29-01-2020)
-----------------------------
- Ultrasonic sensors added.

Requirements:

- In order for the sensors to work properly, "gazebo_ros_pkgs" files must be downloaded to your workspace.

        $ git clone https://github.com/ros-simulation/gazebo_ros_pkgs.git -b melodic-devel

----------------------------------------------------------------------------------
# HAMER_mini v0.3

Changelog v0.3 - (31-01-2020)
---------------------------

-   Added "gazebo_ros_control" to hamer_mini's urdf file.
-   Changed ultrasonic sensors positions and quantities.

# HAMER_mini v0.4

Changelog v0.4 - (01-02-2020)
------------------------------

-   Available SLAM package usage (hamermini_slam.launch).
-   Added laser sensor.
-   Available mapping with laser sensor to gazebo maps.

Requirements:

- In order for the SLAM to work, "slam_gmapping" package must be downloaded to your workspace.
    
        $ git clone https://github.com/ros-perception/slam_gmapping.git -b melodic-devel

SLAM Launching:

        $ roslaunch hamer_mini hamermini_slam.launch

------------------------------------------------------------------------------------------

# HAMER_mini v0.5

Changelog v0.5 - (15-03-2020)
------------------------------

-   Added Hamer Mini's chasis and camera meshes (Camera meshes from Intel Realsense D435, https://github.com/IntelRealSense/librealsense)
-   Added camera module (Image acquisition from the camera has been made possible.)
-   Changed lidar's properties (Lidar is now in tfmini properties.)
-   Added hamer_mini_control package (This package provides communication with Hamer Mini's Arduino controller. Only using with Hamer_Mini Robot, not for simulations).

        $ roslaunch hamer_mini_control hamer_mini_control.launch   
           
-   Added hamer_mini_keyboard package (This package provided Hamer Mini's keyboard controlling.)

        $ rosrun hamer_mini_keyboard hamer_mini_keyboard.py

NOTE: Before running keyboard code, run on terminal this codes:
        
        $ cd ~/hamer_mini_keyboard/scripts
        $ chmod +x hamer_mini_keyboard.py
        
-   Some bug fixes.
--------------------------------------------------------------------------------------------

# HAMER_mini v0.5.1

Changelog v0.5.1 Minor Update - (13.04.2020)
-------------------------------

-   Fixed hamer_mini package's package.xml and CMakeLists.txt files.
-   Fixed "hamermini_gazebo.launch" file. Now, when the gazebo launch file is run alone, the model can be displayed on the screen.
-   Fixed "hamermini_rviz.launch" file. Now all the display tools of the robot come to the rviz menu automatically. Also, when launching the rviz, there is no need to add a "model" to the end of the command.
-   Some changes have been made to the hamer_mini.urdf file. The movement of the wheels was stopped until the problem of wheel movement was resolved (It will be fixed in the next update).
-   Package requirements can now be used by downloading the workspace file to the src folder (such as slam_gmapping and gazebo_ros_pkg).
-   Some bug fixes

NOTE: If you are encountering a freeze problem during the "catkin_make" process, try using the "catkin_make_isolated" command!

--------------------------------------------------------------------------------------------
Contributors: Alim Kerem Erdoğmuş
