cmake_minimum_required(VERSION 3.20)
project(client)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
find_package(sum REQUIRED)

add_executable(client main.cpp)
target_link_libraries(client somthing::sum)