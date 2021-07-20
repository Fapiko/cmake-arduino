cmake_minimum_required(VERSION 3.0.0)

project(sdcard-test CXX)

add_executable(sdcard-test main.cpp)

# Arduino.h is included in hello_world.cpp, so link with Arduino core
target_link_arduino_libraries(sdcard-test PRIVATE core)
target_link_arduino_libraries(sdcard-test PRIVATE SD)

# This is needed for the generation of HEX binary and uploading it
target_enable_arduino_upload(sdcard-test)
