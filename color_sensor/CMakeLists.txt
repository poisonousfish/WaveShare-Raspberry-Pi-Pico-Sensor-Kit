# Generated Cmake Pico project file

cmake_minimum_required(VERSION 3.12)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

# initalize pico_sdk from installed location
# (note this can come from environment, CMake cache etc)
#set(PICO_SDK_PATH "D:/Raspberry/Raspberry_pico/code/pico-sdk")

# Pull in Pico SDK (must be before project)
include(pico_sdk_import.cmake)

project(color_sensor C CXX)

# Initialise the Pico SDK
pico_sdk_init()

# Add executable. Default name is the project name, version 0.1

add_executable(color_sensor color_sensor.c )

pico_set_program_name(color_sensor "color_sensor")
pico_set_program_version(color_sensor "0.1")

pico_enable_stdio_uart(color_sensor 1)
pico_enable_stdio_usb(color_sensor 1)

# Add the standard library to the build
target_link_libraries(color_sensor pico_stdlib)

pico_add_extra_outputs(color_sensor)

