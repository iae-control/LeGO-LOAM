# LeGO-LOAM

This repository contains code for a lightweight and ground optimized lidar odometry and mapping (LeGO-LOAM) system for ROS compatible UGVs. The system takes in point cloud  from a Velodyne VLP-16 Lidar (palced horizontally) and optional IMU data as inputs. It outputs 6D pose estimation in real-time. 

## Dependency

- [ROS](http://wiki.ros.org/ROS/Installation) (tested with indigo, kinetic, and melodic)
- [gtsam](https://github.com/borglab/gtsam/releases) (Georgia Tech Smoothing and Mapping library, 4.0.0-alpha2)
  ```
  wget -O ~/Downloads/gtsam.zip https://github.com/borglab/gtsam/archive/4.0.0-alpha2.zip
  cd ~/Downloads/ && unzip gtsam.zip -d ~/Downloads/
  cd ~/Downloads/gtsam-4.0.0-alpha2/
  mkdir build && cd build
  cmake ..
  sudo make install
  ```

## Compile

You can use the following commands to download and compile the package.

```
cd ~/catkin_ws/src
git clone https://github.com/RobustFieldAutonomyLab/LeGO-LOAM.git
cd ..
catkin_make -j1
```
When you compile the code for the first time, you need to add "-j1" behind "catkin_make" for generating some message types. "-j1" is not needed for future compiling.
