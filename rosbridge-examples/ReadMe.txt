Using ROSbridge

 1. Install rosbridge suite on remote ROS system:
	sudo apt-get install ros-<rosdistro>-rosbridge-suite

2. Run ros node on remote ROS system(On separate terminal):
	roslaunch rosbridge_server rosbridge_websocket.launch

3. Echo the topic to display the received data(On separate terminal):
	rostopic echo /cmd_vel

4. Open this html file on any browser on local machine and send data.

***Must be connected to remote ROS system on local network***
***Make sure to verfiy the IP address of remote ROS system with that used in html files***