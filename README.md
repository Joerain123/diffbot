# DiffBot

DiffBot is an autonomous differential drive robot with two wheels. Its main processing unit is a Raspberry Pi 4 B running Ubuntu Mate 20.04 and the ROS 1 (ROS Noetic) middleware. This respository contains ROS driver packages, ROS Control Hardware Interface for the real robot and configurations for simulating DiffBot. The formatted documentation can be found at: https://fjp.at/projects/diffbot/

| DiffBot | Lidar SLAMTEC RPLidar A2 | RViz |
|:-------:|:-----------------:|:----:|
|  [<img src="https://raw.githubusercontent.com/fjp/diffbot/master/docs/resources/diffbot/diffbot-front.png" width="700">](https://fjp.at/projects/diffbot/) | [<img src="https://raw.githubusercontent.com/fjp/diffbot/master/docs/resources/diffbot/rplidara2.png" width="700">](https://github.com/fjp/diffbot) | [<img src="https://github.com/fjp/diffbot/blob/master/docs/resources/rviz_diffbot_meshes.png?raw=true" width="700">](https://github.com/fjp/diffbot) |

## Package Overview

- `diffbot_base`: ROS Control hardware interface including the controller manager control loop for the real robot
- `diffbot_bringup`: Launch files to bring up the drivers for the real DiffBot robot
- `diffbot_control`: Configurations for the `diff_drive_controller` of ROS Control used in Gazebo simulation and the real robot
- `diffbot_description`: URDF description of DiffBot
- `diffbot_driver`: A reverse ROS bridge for the DiffBot robot (TODO: move driver packages to this ROS package)
- `diffbot_gazebo`: Simulation specific launch and configuration files for DiffBot
- `diffbot_navigation`: move_base launch and configuration files (TODO: tbd)

## DiffBot Control in Gazebo

```console
roslaunch diffbot_control diffbot.launch
```

![DiffBot Gazebo](docs/resources/gazebo/diffbot.png)

## RViz

```console
roslaunch diffbot_description view_diffbot.launch
```

![DiffBot RViz](docs/resources/rviz_diffbot_meshes.png)

## Part List

| SBC RPi 4B | MCU Teensy 3.2 | IMU Bosch |
|:-------:|:-----------------:|:----:|
|  [<img src="https://raw.githubusercontent.com/fjp/diffbot/master/docs/resources/diffbot/sbc-rpi-4b.png" width="700">](https://fjp.at/projects/diffbot/) | [<img src="https://raw.githubusercontent.com/fjp/diffbot/master/docs/resources/diffbot/mcu-teensy32.png" width="700">](https://github.com/fjp/diffbot) | [<img src="https://raw.githubusercontent.com/fjp/diffbot/master/docs/resources/diffbot/imu.png" width="700">](https://github.com/fjp/diffbot) |

| Part                    | Store |
|:------------------------|:---------------------------------------------------------------------------:|
| Raspberry Pi 4 B (4 Gb) | [Amazon.com](https://amzn.to/3ltuJUo), [Amazon.de](https://amzn.to/2IchIAc) |
| SanDisk 64 GB SD Card Class 10 | [Amazon.com](https://amzn.to/2GLOyr0), [Amazon.de](https://amzn.to/3dcFmYE) |
|Robot Smart Chassis Kit  | [Amazon.com](https://amzn.to/34GXNAK), [Amazon.de](https://amzn.to/2Gy3CJ4) |
| SLAMTEC RPLidar A2M8 (12 m) | [Amazon.com](https://amzn.to/3lthTFz), [Amazon.de](https://amzn.to/30MyImR) |
| Grove Ultrasonic Ranger | [Amazon.com](https://amzn.to/36M9TLS), [Amazon.de](https://amzn.to/34GZmyC) |
| Raspi Camera Module V2, 8 MP, 1080p | [Amazon.com](https://amzn.to/2Ib9fgG), [Amazon.de](https://amzn.to/2FdVDQF) |
| Grove Motor Driver | [seeedstudio.com](https://www.seeedstudio.com/Grove-I2C-Motor-Driver-with-L298.html), [Amazon.de](https://amzn.to/36M8O6M) |
| I2C Hub | [seeedstudio.com](https://www.seeedstudio.com/Grove-I2C-Hub.html), [Amazon.de](https://amzn.to/34CGEbz) |


## Additional (Optional) Equipment

| Part                                   | Store |
|:---------------------------------------|:------------------------------------:|
| PicoScope 3000 Series Oscilloscope 2CH | [Amazon.de](https://amzn.to/33I5tUb) |
| VOLTCRAFT PPS-16005                    | [Amazon.de](https://amzn.to/3iKsI4a) |


