file(GLOB IMGUI_SOURCES "*.cpp")
file(GLOB IMPLOT_SOURCES "implot/*.cpp")
file(GLOB IMGUI_BACKENDS_SOURCES "backends/*.cpp")

add_library(imgui ${IMGUI_SOURCES} ${IMPLOT_SOURCES} ${IMGUI_BACKENDS_SOURCES})
target_include_directories(imgui PUBLIC "")
target_include_directories(imgui PUBLIC implot)
target_include_directories(imgui PUBLIC backends)
