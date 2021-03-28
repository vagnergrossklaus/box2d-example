cmake_minimum_required(VERSION 3.5)

project(box2d-example LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

FILE(COPY resources/box.png DESTINATION "${CMAKE_BINARY_DIR}")
FILE(COPY resources/box_jump.png DESTINATION "${CMAKE_BINARY_DIR}")
FILE(COPY resources/ground.png DESTINATION "${CMAKE_BINARY_DIR}")

add_executable(box2d-example src/main.cpp)

target_link_libraries(${PROJECT_NAME}
    PRIVATE Box2D
    PRIVATE sfml-graphics
    PRIVATE sfml-window
    PRIVATE sfml-system
)

