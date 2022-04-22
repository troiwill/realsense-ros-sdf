cmake_minimum_required(VERSION 2.8.3)
project(realsense2_description_sdf)

find_package(catkin REQUIRED COMPONENTS
    )

# RealSense description
catkin_package(
    )

# Install files
install(DIRECTORY launch meshes models rviz
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})

# Tests
# if (CATKIN_ENABLE_TESTING)
#   catkin_add_nosetests(tests)
# endif()