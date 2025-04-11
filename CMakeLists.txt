cmake_minimum_required(VERSION 3.15)
project(miniverse)

set(CMAKE_CXX_STANDARD 17)

# Include directories
include_directories(dependencies/GLFW/include)
include_directories(dependencies/GLEW/include)

# Library directories
link_directories(dependencies/GLFW/lib-vc2019)
link_directories(dependencies/GLEW/lib)

# Create executable
add_executable(miniverse src/main.cpp)

# Link against the actual libraries (IMPORTANT!)
target_link_libraries(miniverse glfw3 glew32 opengl32)