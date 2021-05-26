cmake_minimum_required( VERSION 2.8 )
project( HelloSlam )
list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)

# OpenCV
find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

# Eigen
include_directories("/usr/include/eigen3")

add_executable( GaussNewton GaussNewton.cpp )
target_link_libraries(GaussNewton ${OpenCV_LIBS})

