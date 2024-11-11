cmake_minimum_required(VERSION 3.24)
project(modbus)

set(CMAKE_C_STANDARD 11)

# Find all source files with file extension .c/.cpp inside src folder
file(GLOB_RECURSE PROJECT_SRCS "src/*.c" "src/*.cpp" "src/**/*.c" "src/**/*.cpp")

add_library(modbus STATIC ${PROJECT_SRCS})

# Include project header files
target_include_directories(
        ${PROJECT_NAME}
        PRIVATE src
)
