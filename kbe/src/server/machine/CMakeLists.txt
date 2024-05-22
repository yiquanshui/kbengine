aux_source_directory(. sources)
add_library(Machine ${sources})
target_link_libraries(Machine PRIVATE network common server)
target_include_directories(Machine PRIVATE ..)
