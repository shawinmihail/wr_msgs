cmake_minimum_required(VERSION 2.8.3)
project(wr_msgs)

find_package(catkin REQUIRED
  COMPONENTS
    std_msgs
    sensor_msgs
    nav_msgs
    message_generation
)

add_message_files(
  FILES
    ctrl_stamped.msg
    imu_stamped.msg
    ninelives_triplet_stamped.msg
    steer_stamped.msg
)

generate_messages(
  DEPENDENCIES
    std_msgs
    sensor_msgs
    nav_msgs
)

catkin_package(
  CATKIN_DEPENDS
    std_msgs
    sensor_msgs
    nav_msgs
)
