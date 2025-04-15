cmake_minimum_required(VERSION 3.26)

project(recast_detour LANGUAGES CXX C)

include_directories("./")

file(GLOB SOURCES "ue4-detour.cpp" "UE4RecastHelper.cpp" "Detour/*.h" "Detour/*.cpp")

add_compile_definitions(WITH_NAVMESH_CLUSTER_LINKS)

add_executable(${PROJECT_NAME} ${SOURCES})
