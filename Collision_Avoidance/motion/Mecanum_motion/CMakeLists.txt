cmake_minimum_required(VERSION 2.8.3)
project(Defend_motion)

##using c++ 11 standard
add_definitions(-std=c++11)

##set including directory
set(INCLUDE_DIR
	../common
	../common/cssl
)

##include
include_directories(${INCLUDE_DIR})

add_executable(Mecanum_motion_node 
				motion.cpp 
				motion_nodeHandle.cpp
				base_control.cpp 
				crc_8.cpp
				crc_16.cpp
)
target_link_libraries(Mecanum_motion_node ${catkin_LIBRARIES} csslLib motorDataLib)

