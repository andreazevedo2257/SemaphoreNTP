cmake_minimum_required(VERSION 3.13.0)

project(SemophoreNTP)

add_executable(${PROJECT_NAME} main.cpp)

add_subdirectory(libs/glfw)

target_include_directories(${PROJECT_NAME}
    PUBLIC libs/glfw/include)

target_link_directories(${PROJECT_NAME}
    PRIVATE libs/glfw/src)

target_link_libraries(${PROJECT_NAME}
    glfw)