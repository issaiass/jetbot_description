cmake_minimum_required(VERSION 3.0.2)
project(jetbot_description)

find_package(catkin REQUIRED COMPONENTS
  roslaunch
  urdf
  xacro
)

roslaunch_add_file_check(launch)

catkin_package()

install(
  DIRECTORY launch meshes urdf rviz
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)