cmake_minimum_required(VERSION 3.15)
project(PeBliss)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)


file(GLOB PE_BLISS_SOURCES "src/pe_bliss/*.cpp")

add_library(PeBliss STATIC ${PE_BLISS_SOURCES})

target_include_directories(PeBliss PUBLIC include)

if(WIN32)
    target_compile_definitions(PeBliss PRIVATE /MD)
else()

endif()