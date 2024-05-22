
aux_source_directory(. sources)
find_package(tmxparser COMPONENTS tmxparser)
add_library(Navigation ${sources})
find_package(tinyxml2)
find_package(ZLIB REQUIRED)
target_link_libraries(Navigation PRIVATE common math tmxparser tinyxml2::tinyxml2 ZLIB::ZLIB)