cmake_minimum_required(VERSION 2.6)
project(helloworld)

set( CMAKE_CXX_STANDARD 11 )
set( CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Werror -Ofast")

add_definitions(-DVERSION="${VERSION}")



file(GLOB TUO_SOURCES "helloworld/*.cpp")

enable_language(CXX)
add_executable(helloworld ${TUO_SOURCES})

install(TARGETS helloworld LIBRARY DESTINATION helloworld)
