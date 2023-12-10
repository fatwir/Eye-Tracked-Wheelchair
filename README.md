# Eye Controlled Wheelchair
An innovative technique is used to implement eye tracking to control a wheelchair, the fundamental reason being the assistance of the physically impaired. The user’s eye movements are tracked and are translated into instructions that govern the motion of the wheelchair. When the user looks at the appropriate angle (right, left or centre), the system deciphers it as movements in the corresponding directions. The instruction to turn the system on/off is given when the user blinks twice within a time span of 750 ms. The program was implemented in Python using OpenCV and DLib libraries. The tracking operations were performed on a live video stream captured by the webcam. The average time taken for operations on one frame is around 40 milliseconds, which translates to a frame rate of about 25fps. The working model of the wheelchair is simulated on ROS and Gazebo.

Please find the working demonstration below:<br>
![Demo_gif](https://github.com/fatwir/ETW-Final/assets/81345858/9eaa84d7-740f-40be-8eb1-a49b6a2c8a1f)<br>

# Instructions
Perform the following commands in order to create a ROS workspace once you have installed ROS melodic and gazebo 9.

: mkdir ~/simulation_ws/src -p

: cd ~/simulation_ws/

(Then paste both the packages in the src folder of the workspace and paste the .dat file inside the workspace)


: source /usr/share/gazebo/setup.sh

: source /opt/ros/kinetic/setup.bash

: catkin_make

: source ~/simulation_ws/devel/setup.bash

Now, that the workspace is created copy paste the 2 packageses inside the 'src' folder of the workspace.

run the following command to compile all the packages

: catkin_make

Now, in order to run the simulation, write the following commands on the terminal, each in a new window/tab.

: roslaunch nuric_wheelchair_model_02 wheelchair.launch

: rosrun pkg_ros_basics ETW.py

: rosrun pkg_ros_basics move.py

