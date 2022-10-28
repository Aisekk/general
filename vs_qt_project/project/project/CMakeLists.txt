# CMakeLists.txt for program

cmake_minimum_required(VERSION 3.16.0)

#set(HEADERS .h)
set(SOURCES main.cpp)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${Qt5Widgets_EXECUTABLE_COMPILE_FLAGS} -std=c++1y")

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)

#find_package(Qt5Core REQUIRED)
#find_package(Qt5Gui REQUIRED)
find_package(Qt5Widgets REQUIRED)
#find_package(Qt5Svg REQUIRED)

include_directories(${Qt5Widgets_INCLUDES})
add_executable(${PROJECT_NAME} ${SOURCES}) #${HEADERS}
#qt5_use_modules(main Widgets Core)

#target_link_libraries(${PROJECT_NAME} ${CMAKE_DL_LIBS} 
#	Qt5::Widgets
 #   Qt5::Core
  #  Qt5::Gui
	#Qt5::Svg
	#)

# End file
