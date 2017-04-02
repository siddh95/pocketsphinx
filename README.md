# Modified ROS wrapper for pocketsphinx  
Original repository: https://github.com/mikeferguson/pocketsphinx  
  
Also used repo: https://github.com/gorinars/ros_voice_control  
The script shows how to control ROS turtlebot with English keywords using pocketsphinx.  
It used up-to-date pocketsphinx features and is independent of most external dependencies.  
  
Current repository is a ROS wrapper which incorporates those features.  

## Getting Started
Clone this repository into the src folder of your catkin workspace using:
``` git clone https://github.com/Pankaj-Baranwal/pocketsphinx
```
To know more about catkin workspace and ROS, follow instructions at: http://wiki.ros.org/ROS/Tutorials/InstallingandConfiguringROSEnvironment  
After everything is setup, open a terminal from your catkin workspace and type the following command:  
``` 
catkin_make
```
Now, you are all setup. To test the package:  
1) You should have a dictionary file (with extension ".dict") and a kws list (with extension ".kwlist") ready.  
2) Please ensure that roscore is running.
3) Use the following command to start the required node: (Also add the 2 arguments) 
``` 
rosrun pocketsphinx voice_control_updated.py
```
In case you just want to test the package out, a sample dictionary and kws list have already been placed in the nodes folder within the package. Just use this command:  
``` 
rosrun pocketsphinx voice_control_updated.py _dict:=voice_cmd.dic _kws:=voice_cmd.kwlist
```
For instructions on how to run this node with turlebot simulation, please read the instructions at:  
https://github.com/gorinars/ros_voice_control
