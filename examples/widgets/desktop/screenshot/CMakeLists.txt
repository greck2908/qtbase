# Generated from screenshot.pro.

cmake_minimum_required(VERSION 3.14)
project(screenshot LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

set(INSTALL_EXAMPLEDIR "examples/widgets/desktop/screenshot")

find_package(Qt6 COMPONENTS Core)
find_package(Qt6 COMPONENTS Gui)
find_package(Qt6 COMPONENTS Widgets)

add_qt_gui_executable(screenshot
    main.cpp
    screenshot.cpp screenshot.h
)
target_link_libraries(screenshot PUBLIC
    Qt::Core
    Qt::Gui
    Qt::Widgets
)

install(TARGETS screenshot
    RUNTIME DESTINATION "${INSTALL_EXAMPLEDIR}"
    BUNDLE DESTINATION "${INSTALL_EXAMPLEDIR}"
    LIBRARY DESTINATION "${INSTALL_EXAMPLEDIR}"
)
