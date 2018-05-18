include_directories(
  ${Qt5Widgets_INCLUDE_DIRS}
  ${Qt5Qml_INCLUDE_DIRS}
  ${Qt5Quick_INCLUDE_DIRS}
  ${Qt5QuickControls2_INCLUDE_DIRS}
)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

add_definitions(
  ${Qt5Widgets_DEFINITIONS}
  ${Qt5Qml_DEFINITIONS}
  ${Qt5Quick_DEFINITIONS}
  ${Qt5QuickControls2_DEFINITIONS}
)

file(GLOB sources ${CMAKE_CURRENT_SOURCE_DIR}/*.cc)

set(resources resources.qrc)

qt5_add_resources(resources_RCC ${resources})

set(PROJECT "Example")
project(${PROJECT})

add_executable(${PROJECT}
  ${sources}
  ${resources_RCC}
)

target_link_libraries(${PROJECT}
  Qt5::Widgets
  Qt5::Qml
  Qt5::Quick
  Qt5::QuickControls2
)

