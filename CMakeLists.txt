cmake_minimum_required(VERSION 3.17)
project(qt-digital-clock VERSION 0.1.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Qt6 REQUIRED COMPONENTS Widgets)
qt_standard_project_setup()

qt_add_executable(qt-digital-clock main.cpp
	mainwindow.cpp
	mainwindow.ui)

target_link_libraries(qt-digital-clock PRIVATE Qt6::Widgets)

set_target_properties(qt-digital-clock PROPERTIES
    WIN32_EXECUTABLE ON
    MACOSX_BUNDLE ON
)