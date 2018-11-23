cmake_minimum_required(VERSION 2.8.11)
project(Utilities)

link_directories("/opt/poky-danlaw-v2x/1.8.1/sysroots/cortexa9hf-vfp-neon-poky-linux-gnueabi/usr/lib")

option(WITH_FEATURE_A "Option description" ON)
option(WITH_FEATURE_B "Option description" ON)

if(WITH_FEATURE_A)
  set(CMAKE_UTILITIES_RUN ${CMAKE_CURRENT_SOURCE_DIR}/Run)
  add_subdirectory(${CMAKE_UTILITIES_RUN})
endif()

if(WITH_FEATURE_B)
set(CMAKE_UTILITIES_HALT ${CMAKE_CURRENT_SOURCE_DIR}/Halt)
add_subdirectory(${CMAKE_UTILITIES_HALT})
endif()
