cmake_minimum_required(VERSION 3.2.0)

project(my-sim)

find_package(BioDynaMo REQUIRED)
include(${BDM_USE_FILE})
include_directories("src")

bdm_add_executable(my-sim
                   SOURCES src/my-sim.cc
                   HEADERS src/my-sim.h
                   LIBRARIES ${BDM_REQUIRED_LIBRARIES})
