cmake_minimum_required(VERSION 3.0.2)
project(Original_msgs)

find_package(catkin REQUIRED COMPONENTS
        roscpp
        rospy
        std_msgs
        message_generation
)

add_message_files(
        FILES
        Ping360.msg
        BoundingBox.msg
        BoundingBoxes.msg
)

generate_messages(
        DEPENDENCIES
        std_msgs
)

catkin_package(CATKIN_DEPENDS
        roscpp
        rospy
        std_msgs
        message_runtime
        )

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES Original_msgs
   CATKIN_DEPENDS roscpp rospy std_msgs message_runtime
#  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

