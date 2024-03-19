#########################################################################
#  Project:		Qt Style Plugins for Qt6			#
#  Edit:		19-Mar-24					#
#########################################################################

project(qtstyleplugins6)

set(plastique_SRCS plugin.cpp qplastiquestyle.cpp)
# see https://doc.qt.io/qt-6/qt-add-plugin.html
qt_add_plugin(plastique CLASS_NAME QPlastiqueStyle ${plastique_SRCS})
target_link_libraries(plastique Qt6::Core Qt6::Gui Qt6::Widgets stylecommon)
install(TARGETS plastique DESTINATION ${KDE_INSTALL_PLUGINDIR}/styles)
