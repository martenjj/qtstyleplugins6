#########################################################################
#  Project:		Qt Style Plugins for Qt6			#
#  Edit:		19-Mar-24					#
#########################################################################

project(qtstyleplugins6)

set(cleanlooks_SRCS plugin.cpp qcleanlooksstyle.cpp)
qt_add_plugin(cleanlooks CLASS_NAME QCleanlooksStyle ${cleanlooks_SRCS})
target_link_libraries(cleanlooks Qt6::Core Qt6::Gui Qt6::Widgets stylecommon)
install(TARGETS cleanlooks DESTINATION ${KDE_INSTALL_PLUGINDIR}/styles)
