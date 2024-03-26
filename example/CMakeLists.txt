include(FetchContent)
cmake_minimum_required(VERSION 3.17)

project(example)

set(CMAKE_CXX_STANDARD 17)

FetchContent_Declare(
        imgui-glfw-glad-glm-imguizmo
        GIT_REPOSITORY https://github.com/opsogen/imgui-glfw-glad-glm-imguizmo.git
)
FetchContent_MakeAvailable(imgui-glfw-glad-glm-imguizmo)

add_executable(app main.cpp)

target_link_libraries(
        app
        imgui
        imguizmo
        glm
)
