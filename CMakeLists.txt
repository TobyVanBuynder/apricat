cmake_minimum_required(VERSION 3.13)
project(apricat VERSION 0.1.0 LANGUAGES C CXX)
set(CMAKE_CXX_STANDARD 17)

file(GLOB_RECURSE SOURCE_FILES ${PROJECT_SOURCE_DIR}/src/*.cpp)
add_executable(apricat ${SOURCE_FILES} ${PROJECT_SOURCE_DIR}/src/glad.c)

include_directories(apricat ${PROJECT_SOURCE_DIR}/include)
target_link_libraries(apricat PRIVATE ${PROJECT_SOURCE_DIR}/lib/libglfw3.a)