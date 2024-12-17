cmake_minimum_required(VERSION 3.20.0)
# Project information
project(CPLUSPLUSDEV VERSION 1.0.0 LANGUAGES C CXX)

# Include testing support
include(CTest)
enable_testing()


set(SOURCES
    
)

set(HEADERS
   
)
# add external library eigen3 a math library
set(EXPORT_COMPILE_COMMANDS ON)
find_package(EIGEN3 REQUIRED)


add_library(sum lib/sum.cpp)
target_include_directories(sum PUBLIC include)
# Add executable target
add_executable(CPLUSPLUSDEV src/hello.cpp)
target_link_libraries(CPLUSPLUSDEV sum EIGEN3::Eigen)


# Set C and C++ standards
#set(CMAKE_C_STANDARD 17)
#set(CMAKE_C_STANDARD_REQUIRED True)
# Set the C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)
set_property(TARGET CPLUSPLUSDEV PROPERTY CXX_STANDARD 17)


