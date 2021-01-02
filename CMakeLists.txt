cmake_minimum_required(VERSION 3.9)
project(appveyor)

SET(CMAKE_INCLUDE_PATH ${CMAKE_INCLUDE_PATH} "${CMAKE_CURRENT_SOURCE_DIR}/packages/openssl.1.0.16/build/native/include")
SET(CMAKE_LIBRARY_PATH ${CMAKE_LIBRARY_PATH} "${CMAKE_CURRENT_SOURCE_DIR}/packages/openssl.1.0.16/build/native/Win32/lib")	

SET(CMAKE_INCLUDE_PATH ${CMAKE_INCLUDE_PATH} "${CMAKE_CURRENT_SOURCE_DIR}/packages/protobuf.1.0.5/build/native/include")
SET(CMAKE_LIBRARY_PATH ${CMAKE_LIBRARY_PATH} "${CMAKE_CURRENT_SOURCE_DIR}/packages/protobuf.1.0.5/build/native/lib/Win32")	
SET(CMAKE_PROGRAM_PATH ${CMAKE_PROGRAM_PATH} "${CMAKE_CURRENT_SOURCE_DIR}/packages/protobuf.1.0.5/build/native/bin/Win32")	

add_subdirectory(GameNetworkingSockets)