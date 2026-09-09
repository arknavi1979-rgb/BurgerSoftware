cmake_minimum_required(VERSION 3.15)
project(evilchits)

find_package(imgui CONFIG REQUIRED)

add_library(${PROJECT_NAME} SHARED
    main.cpp
    # your other .cpp files
)

target_link_libraries(${PROJECT_NAME} PRIVATE imgui::imgui)
target_link_libraries(${PROJECT_NAME} PRIVATE d3d11 d3dcompiler dxgi)