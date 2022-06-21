cmake_minimum_required(VERSION 3.21)

set(VCPKG_VERBOSE ON)
set(VCPKG_INSTALL_OPTIONS "--debug" CACHE STRING "")

project(Test LANGUAGES CXX)

find_package(spdlog CONFIG REQUIRED)

add_library(test SHARED Main.cpp)

target_link_libraries(test PRIVATE spdlog::spdlog)
