# Minimum required CMake version
cmake_minimum_required(VERSION 3.10)

# Set the project name
project(logo)

# Add the 'pegtl' library
add_subdirectory(3rd_party/pegtl)

# Include the 'pegtl' header files
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/3rd_party/pegtl/include)

aux_source_directory(src SOURCES)

add_executable(logo ${SOURCES})

target_link_libraries(logo pegtl)

