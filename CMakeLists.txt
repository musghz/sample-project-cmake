# http://derekmolloy.ie/hello-world-introductions-to-cmake
# https://cmake.org/Wiki/CMake/Examples#Set_Include_Directories
# created 13 Jan 2017

cmake_minimum_required(VERSION 3.5.1)
project (gaussianRandomV03cCpp)
set(CMAKE_BUILD_TYPE Release)


#header files
include_directories(include)

#Manually add sources
set(SOURCES src/gaussianRandomV03Cpp.cpp src/gaussRand3.c src/htmlGraphics.c)

#Or use wildcard additions to add sources
#file(GLOB SOURCES "src/*.cpp")

add_executable(gaussianRandomV03cCpp ${SOURCES})

# avoided error but then had issues using make
# to avoid error saying cannot determine linker language for target
#set_target_properties(gaussianRandomV03cCpp PROPERTIES LINKER_LANGUAGE CXX)

# to avoid error saying cannot determine linker language for target
# force g++
set_source_files_properties(${SOURCES} PROPERTIES LANGUAGE CXX)



