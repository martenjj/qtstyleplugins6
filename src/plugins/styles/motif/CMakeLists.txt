#########################################################################
#  Project:		Qt Style Plugins for Qt6			#
#  Edit:		19-Mar-24					#
#########################################################################

project(qtstyleplugins6)

set(motif_SRCS plugin.cpp qmotifstyle.cpp qcdestyle.cpp)
qt_add_plugin(motif CLASS_NAME QMotifStyle ${motif_SRCS})
target_link_libraries(motif Qt6::Core Qt6::Gui Qt6::Widgets stylecommon)
install(TARGETS motif DESTINATION ${KDE_INSTALL_PLUGINDIR}/styles)
