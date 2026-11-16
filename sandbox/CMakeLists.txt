cmake_minimum_required(VERSION 4.2)
project(sandbox)

set(CMAKE_CXX_STANDARD 17)

get_filename_component(BOOST_ROOT_DIR "${CMAKE_CURRENT_SOURCE_DIR}/../../.." ABSOLUTE)

file(GLOB BOOST_INCLUDE_DIRS "${BOOST_ROOT_DIR}/libs/*/include" "${BOOST_ROOT_DIR}/libs/numeric/*/include")


add_executable(sandbox main.cpp)


target_include_directories(sandbox PRIVATE ${BOOST_INCLUDE_DIRS})