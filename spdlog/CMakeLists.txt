project(spdlog)
file(
    GLOB HEADERS
    "*.h"
    "*/*.h"
    "*/*/*.h"
)
file(
    GLOB SOURCES 
    "src/*.cpp"
    "*.cc"
)
add_library(spdlog ${HEADERS} ${SOURCES})
target_compile_definitions(spdlog PUBLIC SPDLOG_COMPILED_LIB)
target_include_directories(spdlog PUBLIC "..")
