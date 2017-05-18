cmake_minimum_required(VERSION 3.6)
project(PeopleTracker)

set(CMAKE_CXX_STANDARD 11)
find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS})

set(SOURCE_FILES main.cpp hungarian.cpp hungarian.h PersonTrack.cpp PersonTrack.h)
add_executable(PeopleTracker ${SOURCE_FILES})

target_link_libraries( PeopleTracker ${OpenCV_LIBS} )

