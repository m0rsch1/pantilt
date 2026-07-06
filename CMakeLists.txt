###
# Generated CMakeLists.txt from app.py
# Many
# 2026-07-06
#
# When called, cmake will generate an assembled SMURF file (and other artifacts like URDF/SDF) from a SMURFA (Arrangement) file
###

cmake_minimum_required(VERSION 3.10)
project(PanTiltUnit)

add_custom_command(OUTPUT ${CMAKE_CURRENT_SOURCE_DIR}/smurf/PanTiltUnit.smurf COMMAND phobos convert ${CMAKE_CURRENT_SOURCE_DIR}/PanTiltUnit.smurfa ${CMAKE_CURRENT_SOURCE_DIR}/.)
# TODO: It is maybe a good idea to call xrock-add-hardware-model here
add_custom_target(build_PanTiltUnit ALL DEPENDS ${CMAKE_CURRENT_SOURCE_DIR}/smurf/PanTiltUnit.smurf)

# Empty install target for autoproj
install(FILES DESTINATION)