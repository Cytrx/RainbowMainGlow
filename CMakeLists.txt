cmake_minimum_required(VERSION 3.17)
project(RainbowMainGlow)

add_library(${PROJECT_NAME} SHARED
    src/RainbowMainGlow.cpp
)

target_include_directories(${PROJECT_NAME} PRIVATE
    include
    ${CMAKE_INSTALL_PREFIX}/include
)

target_link_libraries(${PROJECT_NAME}
    ${CMAKE_INSTALL_PREFIX}/lib/libGeodeLib.a
)

set_target_properties(${PROJECT_NAME} PROPERTIES
    LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin
)
