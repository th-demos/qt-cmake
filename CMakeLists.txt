cmake_minimum_required(VERSION 3.16)

add_subdirectory(cmake_tools)
ensure_vcpkg()

project(qt-cmake)

find_package(Qt6 CONFIG REQUIRED COMPONENTS Core Widgets)

add_executable(qt-cmake src/main.cc src/mainwindow.cc)
target_link_libraries(qt-cmake PRIVATE Qt6::Core Qt6::Widgets)