
aux_source_directory(. sources)
add_library(server STATIC ${sources})
target_include_directories(server PUBLIC .. PRIVATE .)
target_link_libraries(server PUBLIC pyscript fmt PRIVATE xml network)

