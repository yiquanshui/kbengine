
aux_source_directory(. sources)
add_library(network ${sources})
target_include_directories(network PUBLIC .)
target_link_libraries(network PRIVATE common)