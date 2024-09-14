cmake_minimum_required(VERSION 3.22)

project(
    compiler
    VERSION 0.1
    LANGUAGES CXX
)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_executable(compiler)
target_include_directories(compiler PUBLIC src)
target_compile_features(compiler PUBLIC cxx_std_20)
set_target_properties(compiler PROPERTIES CXX_EXTENSIONS OFF)
target_compile_options(compiler PRIVATE -Wall -Wextra -Wno-unused-variable -Wno-unused-private-field -Wno-unused-parameter -Werror)

add_subdirectory(src)
