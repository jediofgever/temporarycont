## Installing ROS

Setup your computer to accept software from packages.ros.org. 

 > sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

Set up your keys

 > sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
 
Make sure your Debian package index is up-to-date: 
 > sudo apt-get update

Install full ROS version: 
 > sudo apt-get install ros-kinetic-desktop-full
(Note: When installing make sure openCV is NOT between the requested packages)

Before you can use ROS, you will need to initialize rosdep. rosdep enables you to easily install system dependencies for source you want to compile and is required to run some core components in ROS:
 > sudo rosdep init

 > rosdep update
 
It's convenient if the ROS environment variables are automatically added to your bash session every time a new shell is launched: 
 > echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
 > source ~/.bashrc

## Installing Gazebo 8

Setup the packages list: 

 > List item sudo sh -c 'echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable \`lsb_release -cs\` main" > /etc/apt/sources.list.d/gazebo-stable.list'
 
Set up your keys
 > wget http://packages.osrfoundation.org/gazebo.key -O - | sudo apt-key add -

Make sure your Debian package index is up-to-date: 

 > sudo apt-get update
 
Install gazebo 8 and dependencies following next order: 
 > sudo apt-get install libignition-math3 

 > sudo apt-get install gazebo8

 > sudo apt-get install ros-kinetic-gazebo8-ros-pkgs


## Additional requirements

ROS packages: 

 > sudo apt-get install ros-kinetic-fake-localization ros-kinetic-joy ros-kinetic-voxel-grid ros-kinetic-map-server

 > sudo apt-get  install libignition-transport4 libignition-transport4-dev libignition-msgs0-dev

ROS control:

 > sudo apt-get install ros-kinetic-gazebo8-ros-control ros-kinetic-controller-manager ros-kinetic-position-controllers  ros-kinetic-joint-state-controller  ros-kinetic-effort-controllers ros-kinetic-laser-geometry ros-kinetic-joint-state-controller ros-kinetic-joint-state-publisher
