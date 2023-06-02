find_package(Qt5Core)
find_package(Qt5Gui)
find_package(Qt5Widgets)
find_package(Qt5OpenGL)
find_package(Qt5Svg)

qt5_add_resources(qrc svgviewer.qrc)
add_executable(svg_viewer
   main.cpp
   mainwindow.h
   mainwindow.cpp
   svgview.h
   svgview.cpp
   exportdialog.h
   exportdialog.cpp
   ${qrc}
   )

set_target_properties(svg_viewer PROPERTIES AUTOMOC ON)
target_link_libraries(svg_viewer
   Qt5::Widgets
   Qt5::Gui
   Qt5::Svg
   Qt5::OpenGL
   )

