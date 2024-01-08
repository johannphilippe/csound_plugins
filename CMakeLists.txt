cmake_minimum_required(VERSION 3.19)

project(csound_plugins LANGUAGES CXX)
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_SOURCE_DIR}/cmake/Modules/)


option(BUILD_HYPERCURVE "Build Csound opcodes" ON)
option(BUILD_LUA_CSOUND "Build Lua for Csound opcodes" ON)
option(BUILD_RAWMIDI "Build rawmidi - RtMidi for Csound - opcodes" ON)

if(BUILD_HYPERCURVE)
    add_subdirectory(hypercurve)
endif()

if(BUILD_LUA_CSOUND)
    add_subdirectory(lua_csound)
endif()

if(BUILD_RAWMIDI) 
    add_subdirectory(rawmidi_csound)
endif()
