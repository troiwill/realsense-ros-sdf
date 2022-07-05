# realsense-ros-sdf
ROS package for SDF versions of the RealSense camera models. We tested the following models using ROS Melodic and Gazebo 9 on Ubuntu 18.

## Installation

Install the Intel RealSense camera description.
```
sudo apt install ros-melodic-realsense2-description
```

Clone the realsense gazebo plugin repository and create a link to it.
```
mkdir -p ${HOME}/repos && cd ${HOME}/repos
git clone https://github.com/troiwill/realsense_gazebo_plugin
cd ${HOME}/catkin_ws/src
ln -s ${HOME}/repos/realsense_gazebo_plugin realsense_gazebo_plugin
```

Clone this repository.
```
# Downloading converted SDF cameras.
mkdir -p ${HOME}/repos && cd ${HOME}/repos
git clone https://github.com/troiwill/realsense-ros-sdf.git
cd realsense-ros-sdf
```

Finally, add the models to your catkin workspace. To add the models to your catkin workspace, you can either use a symbolic link (option 1) or copy the description directory directly (option 2).

**Option 1: (Recommended)**
```
cd ${HOME}/catkin_ws/src
ln -s ${HOME}/repos/realsense-ros-sdf/realsense2_description_sdf realsense2_description_sdf
```

**Option 2:**
```
cd ${HOME}/catkin_ws/src
cp -r ${HOME}/repos/realsense-ros-sdf/realsense2_description_sdf .
```

After either option, run `catkin build` in the root workspace directory (i.e., `${HOME}/catkin_ws`).
```
cd ${HOME}/catkin_ws
catkin build
```
