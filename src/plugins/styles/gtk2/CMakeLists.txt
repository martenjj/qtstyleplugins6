#########################################################################
#  Project:		Qt Style Plugins for Qt6			#
#  Edit:		19-Mar-24					#
#########################################################################

project(qtstyleplugins6)

set(gtk2_SRCS plugin.cpp qgtk2painter.cpp qgtkpainter.cpp qgtkstyle.cpp qgtkstyle_p.cpp plugin.cpp)
qt_add_plugin(gtk2 CLASS_NAME QGtk2Style ${gtk2_SRCS})
include_directories(${GTK2_INCLUDE_DIRS})
target_link_libraries(gtk2 Qt6::Core Qt6::Gui Qt6::Widgets Qt6::WidgetsPrivate stylecommon ${GTK2_LIBRARIES} X11)
install(TARGETS gtk2 DESTINATION ${KDE_INSTALL_PLUGINDIR}/styles)
