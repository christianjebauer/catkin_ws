cmake_minimum_required(VERSION 3.0.2)

## Compile as C++11, supported in ROS Kinetic and newer
add_compile_options(-std=c++11)

include_directories(${ROS_LIB_DIR})

generate_arduino_firmware(button
  SRCS button_led.cpp ${ROS_LIB_DIR}/time.cpp
  BOARD nano328
  PORT /dev/ttyUSB0
)

