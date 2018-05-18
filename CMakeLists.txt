cmake_minimum_required(VERSION 2.8)

find_package(Qt5
    COMPONENTS
      Widgets
      Qml
      Quick
      QuickControls2
    REQUIRED)

add_subdirectory(src)

