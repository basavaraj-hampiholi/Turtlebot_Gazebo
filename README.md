# Step by step installation of turtlebot using Gazebo UI on ROS platform
1. Installation of ROS.
    Turtlebot is supported by Indigo version of the ROS. Indigo version requires Ubuntu 14.04 LTS. The following link 
    explain the installation of indigo version of ROS in Ubuntu 14.04 LTS.
    http://wiki.ros.org/indigo/Installation/Ubuntu
    Please choose the Desktop-Full Install option which is recommended one. 



2. After successfull installation of ROS(indigo), we now install TurtleBot packages. Please copy the below link into 
  terminal and execute.

      sudo apt-get install ros-indigo-turtlebot ros-indigo-turtlebot-apps ros-indigo-turtlebot-interactions 
      ros-indigo-turtlebot-simulator ros-indigo-kobuki-ftdi ros-indigo-rocon-remocon ros-indigo-rocon-qt-library 
      ros-indigo-ar-track-alvar-msgs

   Test the TurtleBot installation by running the command:$ roscore. This will give you, 
    started core service [/rosout] 
   if installed correctly. 
   you should start and keep this up whenever you use TurtleBot.


3. Simulation

3.1 Gazebo: Now we will make operations on TurtleBot in Gazebo GUI which provides overview about the environment 
    to the robot. First launch Gazebo by executing the below command on new terminal,
         roslaunch turtlebot_gazebo turtlebot_world.launch
      
    You can find more information about Gazebo in 
     http://gazebosim.org/tutorials?cat=guided_b&tut=guided_b2
   
3.2 Rviz: viz is a 3D visualization environment for the ROS. While Gazebo is running, 
     launch Rviz in a new terminal:
    
         roslaunch turtlebot_rviz_launchers view_robot.launch
   
     You would see a TurtleBot.
   



 
    
