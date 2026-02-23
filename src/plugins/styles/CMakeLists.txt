#########################################################################
#  Project:		Qt Style Plugins for Qt6			#
#  Edit:		23-Feb-26					#
#########################################################################

project(qtstyleplugins6)

#########################################################################
#  Dependencies								#
#########################################################################

if (BUILD_GTK2_STYLE)
  find_package(GTK2 2.0 COMPONENTS gtk)
endif ()

#########################################################################
#  The shared headers and static library				#
#########################################################################

add_subdirectory(shared)

#########################################################################
#  Styles								#
#########################################################################

add_subdirectory(plastique)
add_subdirectory(motif)
add_subdirectory(cleanlooks)
if (BUILD_GTK2_STYLE AND GTK2_FOUND)
  add_subdirectory(gtk2)
endif ()
if (BUILD_BB10_STYLE)
  add_subdirectory(bb10style)
endif ()
