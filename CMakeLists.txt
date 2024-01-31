cmake_minimum_required(VERSION 3.20)

project(my-cpp-nvim)

add_executable(main main.cpp Sub.cpp)
target_include_directories(main PRIVATE .)

target_compile_features(main PRIVATE cxx_std_20)

