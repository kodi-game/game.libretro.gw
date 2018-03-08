cmake_minimum_required(VERSION 3.1)
project(game.libretro.gw)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-gw REQUIRED)

set(GW_CUSTOM_BINARY ${GW_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} GW "")

include(CPack)
