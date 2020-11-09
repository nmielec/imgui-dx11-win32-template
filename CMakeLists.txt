cmake_minimum_required(VERSION 3.13)

project (ImGui-base-gui)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CXX_EXTENSIONS NO)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_HOME_DIRECTORY}/bin)

add_subdirectory(imgui)

add_executable(gui src/main.cpp)

target_compile_options(gui PUBLIC -Wall -Wextra -pedantic)

target_include_directories(gui PUBLIC imgui)
target_include_directories(gui PUBLIC imgui/backends)
target_include_directories(gui PUBLIC imgui/implot)
target_link_libraries(gui imgui xinput1_4 d3d11 d3dcompiler_47)

