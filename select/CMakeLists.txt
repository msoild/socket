cmake_minimum_required(VERSION 2.8.7)
project(socketSelect)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -pthread -std=c++11")

include_directories(
     ./src
)
#compile server
add_executable(${PROJECT_NAME}Server
    src/selectServer.cpp
)
#target_link_libraries(${PROJECT_NAME}Server
#  PRIVATE
#    CommonAPI
#    CommonAPI-SomeIP
#    vsomeip
#)

#compile client binary
add_executable(${PROJECT_NAME}Client
    src/selectClient.cpp
)
#target_link_libraries(${PROJECT_NAME}Client
#  PRIVATE
#    CommonAPI
#    CommonAPI-SomeIP
#    vsomeip
#)

