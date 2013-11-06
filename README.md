IMU tools for ROS
===================================

Overview
-----------------------------------

IMU-related filters and visualizers. The stack contains:

 * `imu_filter_madgwick`: a filter which fuses angular velocities,
accelerations, and (optionally) magnetic readings from a generic IMU 
device into an orientation. Based on the work of [1].

 * `rviz_imu_plugin` a plugin for rviz which displays `sensor_msgs::Imu`
messages

Installing
-----------------------------------

### From source ###

Create a directory where you want the package downloaded (ex. `~/ros`), 
and add it to `$ROS_PACKAGE_PATH`.

Make sure you have git installed:

    sudo apt-get install git-core

Download the stack from our repository:

    git clone https://github.com/ccny-ros-pkg/imu_tools.git

Checkout branch corresponding to your ros version.

Install any dependencies using [rosdep](http://www.ros.org/wiki/rosdep).

    rosdep install imu_tools

Compile the stack:

    rosmake imu_tools

Troubleshooting
-----------------------------------

If you run into trouble using `rosdep install imu_tools`:

    ERROR: the following packages/stacks could not have their rosdep keys resolved
    to system dependencies:
    rviz_imu_plugin: Missing resource cmake_modules

Resolve with:

    sudo apt-get install ros-hydro-cmake-modules


More info
-----------------------------------

http://ros.org/wiki/imu_tools

License
-----------------------------------

 * `imu_filter_madgwick`: currently licensed as GPL, following the original implementation

 * `rviz_imu_plugin`: BSD

References
-----------------------------------
 [1] http://www.x-io.co.uk/node/8#open_source_ahrs_and_imu_algorithms