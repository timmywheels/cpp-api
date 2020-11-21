cmake_minimum_required(VERSION 3.12)
project(cpp-api)

set(CMAKE_CXX_STANDARD 14)
# see https://cmake.org/cmake/help/latest/module/FindBoost.html
find_package(Boost REQUIRED)

include_directories(${Boost_INCLUDE_DIR})
add_executable(${PROJECT_NAME} src/main.cpp)

# see https://cmake.org/cmake/help/latest/module/FindBoost.html
find_package(Boost REQUIRED COMPONENTS components you would like to link with)
include_directories(${Boost_INCLUDE_DIR})
# Note: a target should be already defined using 'add_executable' or 'add_library' 
target_link_libraries(src/main.cpp ${Boost_LIBRARIES})