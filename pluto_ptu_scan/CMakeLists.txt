cmake_minimum_required(VERSION 2.8.3)
project(pluto_ptu_scan)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  sensor_msgs
  std_msgs
  tf
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES pluto_costmap_generator
#  CATKIN_DEPENDS pcl_ros roscpp rospy sensor_msgs std_msgs tf
#  DEPENDS system_lib
)


include_directories(
  ${catkin_INCLUDE_DIRS}
)

include_directories(include ${catkin_INCLUDE_DIRS})

add_executable(pluto_ptu_scan src/tilt_motion.cpp)

target_link_libraries(pluto_ptu_scan
  ${catkin_LIBRARIES}
)
