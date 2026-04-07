cmake_minimum_required(VERSION 3.10)
project(RayTracing)

set(CMAKE_CXX_STANDARD 17)

add_executable(RayTracing main.cpp Object.hpp Vector.hpp Sphere.hpp global.hpp Triangle.hpp Scene.cpp Scene.hpp Light.hpp Renderer.cpp)
target_compile_features(RayTracing PUBLIC cxx_std_17)

if(MSVC)
	target_compile_options(RayTracing PRIVATE /W4)
else()
	target_compile_options(RayTracing PRIVATE -Wall -Wextra -pedantic -Wshadow -Wreturn-type)
	target_compile_options(RayTracing PRIVATE -fsanitize=undefined)
	target_link_options(RayTracing PRIVATE -fsanitize=undefined)
endif()
