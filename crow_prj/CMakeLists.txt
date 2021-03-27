cmake_minimum_required(VERSION 3.7)

project(crow_prj)

set(CMAKE_CXX_STANDARD 11)
set(THREADS_PREFER_PTHREAD_FLAG_ON)

find_package(Boost COMPONENTS system filesystem REQUIRED)
find_package(Threads)

include_directories(${Boost_INCLUDE_DIRS})
add_executable(crow_prj main.cpp)
target_link_libraries(crow_prj ${Boost_LIBRARIES} Threads::Threads)