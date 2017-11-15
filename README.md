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

  a. Gazebo: Now we will make operations on TurtleBot in Gazebo GUI which provides overview about the environment 
    to the robot. First launch Gazebo by executing the below command on new terminal,
    
         roslaunch turtlebot_gazebo turtlebot_world.launch
      
    You can find more information about Gazebo in 
    
        http://gazebosim.org/tutorials?cat=guided_b&tut=guided_b2
   
  b. Rviz: viz is a 3D visualization environment for the ROS. While Gazebo is running, 
     launch Rviz in a new terminal:
    
         roslaunch turtlebot_rviz_launchers view_robot.launch
   
     You would see a TurtleBot. Now the turtlebot is ready for simulation.
  
# Creating simulation world, Map building and Navigation of TurtleBot:
  1. Create world:  To create the world for turtlebot, first launch the Gazebo with empty world. Then go to insert tab 
     and add the different objects to world. Finally, save as filename.world. 
  
  
  2. Create map: To create a map, first launch the gazebo world saved in previous step. Then launch the Rviz for navigation.
     Now you can see Rviz navigation window. To interact with keyboard, launch the turtlebot_teleop for keyboard. You can
     also use other interactive markers like mouse to control the robot movement. Make movements using these markers and
     create the map in the world. Save this map using:
         
         rosrun map_server map_saver -f /home/<user_name>/turtlebot_custom_maps/tutorial
         
   3. Navigation: First launch the world created by you and then load the map file as per the tutorial. Go to Rviz navigation
      window and select the 2D Nav Goal button. Now click on the map to drive the turtlebot to that particular location. 
      You can drive the turtlebot to particular location using go_to_specific_point_on_map.py. Click on 'Publish Point' 
      button and place it on map(do not click), note down firtst two coordinate points(X,Y) at left below corner and 
      then click. Now, open the file go_to_specific_point_on_map.py in editor and edit the X and Y location 
      in code(line# 83). Run the code using python. Now you can see the turtlebot moving towards the destination. Once the
      turtlebot is reached destination, you will be notified that "reached destination" and stops there. Do select the points
      within the map, else the turtlebot fails to reach the desired pose.
      
                
     
  
   



 
    
