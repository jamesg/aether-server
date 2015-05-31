cmake_minimum_required(VERSION 2.8)

project("Aether Server")
enable_testing()

find_package(CURL)
find_package(Threads)
find_package(OpenSSL)
find_package(Boost COMPONENTS date_time filesystem random regex system thread)

include_directories("aether/include")
include_directories("atlas/lib/mongoose/include")
include_directories("atlas/include")
include_directories("commandline/include")
include_directories("hades/include")
include_directories("hades/lib/sqlite3/include")

add_definitions("-std=c++11")

add_subdirectory(hades)
add_subdirectory(atlas)
add_subdirectory(aether)

