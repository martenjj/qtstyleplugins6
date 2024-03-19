#########################################################################
#  Project:		KDE - "Bakelite" style				#
#  Edit:		18-Mar-24					#
#  SCCS:		<%Z% %M% %I%>			#
#########################################################################
#									#
#									#
#########################################################################

project(qtstyles)

#########################################################################
#									#
#  Common style library							#
#									#
#########################################################################

set(stylecommon_SRCS qstylehelper.cpp)
add_library(stylecommon STATIC ${stylecommon_SRCS})
target_link_libraries(stylecommon Qt::Core Qt::Widgets)
