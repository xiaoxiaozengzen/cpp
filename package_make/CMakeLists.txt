project(myapp)
cmake_minimum_required(VERSION 2.8)


SET(CMAKE_PREFIX_PATH ${CMAKE_PREFIX_PATH} "${CMAKE_CURRENT_SOURCE_DIR}/mylib/Install")
find_package(mylib REQUIRED)
if(mylib_FOUND)
	message(STATUS "mylib_FOUND = ${mylib_FOUND}")
endif()

message(STATUS "mylib_DIR = ${mylib_DIR}")
message(STATUS "mylib_INCLUDE_DIRECTORIES = ${mylib_INCLUDE_DIRECTORIES}")
message(STATUS "mylib_LIBRARIES = ${mylib_LIBRARIES}")
message(STATUS "mylib_SOURCES = ${mylib_SOURCES}")

add_executable(${PROJECT_NAME} myapp.cpp)
target_link_libraries(${PROJECT_NAME} mylib::mylib)
