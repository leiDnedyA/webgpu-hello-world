cmake_minimum_required(VERSION 3.0...3.25)
project(
    LearnWebGPU
    VERSION 0.1.0
    LANGUAGES CXX C
)
add_subdirectory(webgpu)
add_executable(App main.cpp)
target_link_libraries(App PRIVATE webgpu)
target_copy_webgpu_binaries(App)
