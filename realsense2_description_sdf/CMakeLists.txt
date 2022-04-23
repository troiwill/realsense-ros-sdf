cmake_minimum_required(VERSION 3.0.2)
project(realsense2_description_sdf)

find_package(catkin REQUIRED COMPONENTS
  gazebo_ros
)

find_package(gazebo_ros REQUIRED)

catkin_package(
  DEPENDS
)

# Install files
install(DIRECTORY launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(DIRECTORY meshes
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(DIRECTORY rviz
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(DIRECTORY models
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

# Tests
# if (CATKIN_ENABLE_TESTING)
#   catkin_add_nosetests(tests)
# endif()