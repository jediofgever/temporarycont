## Start IMU Xsens

> sudo chmod 777 /dev/ttyUSB0

> roslaunch xsens_driver xsens_driver.launch\

## Multi Velodyne launch

> roslaunch velodyne_pointcloud VLP16_multi.launch

## Record Bag

> rosbag record /horizontal/velodyne_points /vertical/velodyne_points /imu

## Launch Cartogpaher

>  roslaunch cartographer_ros demo_backpack_3d.launch bag_filename:=${HOME}/Downloads/2019-02-13-16-02-36.bag

## Run offline mapping cartogrpher node
>  roslaunch cartographer_ros offline_backpack_3d.launch bag_filenames:=${HOME}/Downloads/2019-02-13-21-21-48.bag

## create map picture
>  roslaunch cartographer_ros assets_writer_backpack_3d.launch    bag_filenames:=${HOME}/Downloads/2019-02-13-21-21-48.bag    pose_graph_filename:=${HOME}/Downloads/2019-02-13-21-21-48.bag.pbstream
