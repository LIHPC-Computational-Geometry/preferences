include (${CMAKE_SOURCE_DIR}/cmake/version.cmake)
include (${CMAKE_SOURCE_DIR}/cmake/common.cmake)
include (${CMAKE_SOURCE_DIR}/cmake/workarounds.cmake)

#find_package (Qt5Widgets 5.9.1 REQUIRED)

add_executable (create_tree create_tree.cpp)
add_executable (read_config read_config.cpp)

target_include_directories (create_tree PRIVATE ../PrefsXerces/public ../PrefsCore/public)
target_include_directories (read_config PRIVATE ../PrefsXerces/public ../PrefsCore/public)
target_link_libraries (create_tree PUBLIC PrefsXerces)
target_link_libraries (read_config PUBLIC PrefsXerces)

