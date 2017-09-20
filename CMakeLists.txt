cmake_minimum_required(VERSION 2.8.7)

project(main)

set(PROJECT_VERSION_MAJOR 1)
set(PROJECT_VERSION_MINOR 1)
set(PROJECT_VERSION_PATCH 0)
set(PROJECT_VERSION "${PROJECT_VERSION_MAJOR}.${PROJECT_VERSION_MINOR}.${PROJECT_VERSION_PATCH}")

add_compile_options(-std=c++11)
set(MAIN_SOURCES
    main.cpp
)

add_executable(main ${MAIN_SOURCES})
set_target_properties(main PROPERTIES COMPILE_FLAGS "-DHKT_BIG_ENDIAN")
install(TARGETS main RUNTIME DESTINATION usr/bin)
