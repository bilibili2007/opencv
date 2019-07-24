# cmake needs this line
cmake_minimum_required(VERSION 3.1)

# Enable C++11
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)

# Define project name
project(displayImage)

# Find OpenCV, you may need to set OpenCV_DIR variable
# to the absolute path to the directory containing OpenCVConfig.cmake file
# via the command line or GUI
find_package(OpenCV REQUIRED)


# Declare the executable target built from your sources
add_executable(displayImage displayImage.cpp)

# Link your application with OpenCV libraries
target_link_libraries(displayImage ${OpenCV_LIBS})
