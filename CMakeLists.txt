cmake_minimum_required(VERSION 3.0.2)
project(telegram_ros)


find_package(catkin REQUIRED COMPONENTS
  rospy
  std_msgs
)

catkin_package()

#############
## Install ##
#############

install(PROGRAMS 
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

install(DIRECTORY
  launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

catkin_install_python(PROGRAMS
  script/telegram_node
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

