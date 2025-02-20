cmake_minimum_required(VERSION 3.15)
project(coop-mat)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_subdirectory(${CMAKE_HOME_DIRECTORY}/ext/vk-bootstrap)
add_executable(coop_vulkan 
    src/vulkan/driver.cpp
)

target_link_libraries(coop_vulkan vk-bootstrap::vk-bootstrap)