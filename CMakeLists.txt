cmake_minimum_required(VERSION 3.9)
project(appveyor)

set(OPENSSL_USE_STATIC_LIBS True)

set(CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake")	

SET(CMAKE_INCLUDE_PATH ${CMAKE_INCLUDE_PATH} "${CMAKE_CURRENT_SOURCE_DIR}/packages/openssl.1.0.23/build/native/include")
SET(CMAKE_LIBRARY_PATH ${CMAKE_LIBRARY_PATH} "${CMAKE_CURRENT_SOURCE_DIR}/packages/openssl.1.0.23/build/native/Win32/lib")	

SET(CMAKE_INCLUDE_PATH ${CMAKE_INCLUDE_PATH} "${CMAKE_CURRENT_SOURCE_DIR}/packages/protobuf.1.0.5/build/native/include")
SET(CMAKE_LIBRARY_PATH ${CMAKE_LIBRARY_PATH} "${CMAKE_CURRENT_SOURCE_DIR}/packages/protobuf.1.0.5/build/native/lib/Win32")	
SET(CMAKE_PROGRAM_PATH ${CMAKE_PROGRAM_PATH} "${CMAKE_CURRENT_SOURCE_DIR}/packages/protobuf.1.0.5/build/native/bin/Win32")	

message(${OPENSSL_USE_STATIC_LIBS})
add_subdirectory(GameNetworkingSockets)
