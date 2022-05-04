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
find_package(Threads REQUIRED)
add_library(spdlog ${HEADERS} ${SOURCES})
set_target_properties(spdlog PROPERTIES LINKER_LANGUAGE CXX)
target_link_libraries(spdlog PUBLIC Threads::Threads)
target_include_directories(spdlog PUBLIC "..")
