#########################################################################
#  Project:		Qt Style Plugins for Qt6			#
#  Edit:		19-Mar-24					#
#########################################################################
#									#
#  Style sources updated for Qt6 and adapted to build with ECM/CMake.	#
#  Originally from https://code.qt.io/cgit/qt/qtstyleplugins.git	#
#									#
#########################################################################

project(qtstyleplugins6)
cmake_minimum_required(VERSION 3.16)

#########################################################################
#  Dependencies								#
#########################################################################

set(QT_MIN_VERSION "6.5.0")
set(ECM_MIN_VERSION "6.0.0")

find_package (ECM ${ECM_MIN_VERSION} REQUIRED NO_MODULE)
set (CMAKE_MODULE_PATH ${ECM_MODULE_PATH})

include(KDEInstallDirs)
include(KDECompilerSettings NO_POLICY_SCOPE)
include(KDECMakeSettings)
include(FeatureSummary)
include(ECMSetupVersion)

find_package(Qt6 ${QT_MIN_VERSION} CONFIG REQUIRED COMPONENTS Core Gui Widgets)

#########################################################################
#  Rigourousness							#
#########################################################################

add_definitions("-DQT_USE_FAST_CONCATENATION")
add_definitions("-DQT_USE_FAST_OPERATOR_PLUS")
add_definitions("-DQT_NO_CAST_FROM_BYTEARRAY")
add_definitions("-DQT_NO_URL_CAST_FROM_STRING")
add_definitions("-DQT_NO_CAST_TO_ASCII")
add_definitions("-DQT_NO_FOREACH")

remove_definitions("-DQT_NO_CAST_FROM_ASCII")
remove_definitions("-DQT_NO_SIGNALS_SLOTS_KEYWORDS")
remove_definitions("-DQT_NO_KEYWORDS")

#########################################################################
#  Subdirectories							#
#########################################################################

add_subdirectory(src)

#########################################################################
#  Information at end of configuration					#
#########################################################################

feature_summary(WHAT ALL FATAL_ON_MISSING_REQUIRED_PACKAGES)
