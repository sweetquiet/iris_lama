cmake_minimum_required(VERSION 3.5)
project(iris_lama)

set(CMAKE_CXX_STANDARD 11) # use c++11

# Default to release mode.
if (NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE Release)
endif()

find_package(catkin REQUIRED COMPONENTS
    roscpp
)

catkin_package()

add_subdirectory(src)

export(TARGETS iris-lama FILE iris_lamaConfig.cmake)

set(CMAKE_EXPORT_PACKAGE_REGISTRY ON)
export(PACKAGE iris_lama)

