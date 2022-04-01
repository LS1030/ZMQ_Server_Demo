cmake_minimum_required(VERSION 3.10)
project(ZMQ_Server_Demo)

set(CMAKE_CXX_STANDARD 14)

# Inc
include_directories(./Inc)
include_directories(./3rd_party/cppzmq)

# Src
aux_source_directory(./Src/ USER_SRC)

# bin
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/bin)

add_executable(ZMQ_Server_Demo ${USER_SRC})
target_link_libraries(ZMQ_Server_Demo zmq)
