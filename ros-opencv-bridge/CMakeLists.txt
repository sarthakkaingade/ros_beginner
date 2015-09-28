cmake_minimum_required(VERSION 2.8.3)
project(ros_opencv_bridge)

## Find catkin and any catkin packages
find_package(catkin REQUIRED COMPONENTS roscpp rospy std_msgs genmsg sensor_msgs cv_bridge image_transport)

## Declare a catkin package
catkin_package()

## Build talker and listener
include_directories(include ${catkin_INCLUDE_DIRS})

add_executable(ros_opencv_bridge src/ros_opencv_bridge.cpp)
target_link_libraries(ros_opencv_bridge ${catkin_LIBRARIES})
add_dependencies(ros_opencv_bridge ros_opencv_bridge_generate_messages_cpp)
