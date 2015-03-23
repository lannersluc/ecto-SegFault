# ecto-SegFault

# How to provoke the segFault:

To install ecto and ORK follow these steps: \n
1.) mkdir ws && cd ws
2.) export DISTRO=hydro
3. )sudo apt-get install libopenni-dev ros-${DISTRO}-catkin ros-${DISTRO}-ecto* ros-${DISTRO}-opencv-candidate ros-${DISTRO}-moveit-msgs
4.) source /opt/ros/${DISTRO}/setup.sh
5.) Copy the file "ros.rosinstall" into the ws directory
6.) wstool init src ros.rosinstall
7.) cd src && wstool update -j8
8.) cd .. && rosdep install --from-paths src -i -y
9.) catkin_make
10.) source devel/setup.bash

After compilation, run the following command to provoke segFault:
11.) roslaunch object_detection filtered_kinect_detection.launch

