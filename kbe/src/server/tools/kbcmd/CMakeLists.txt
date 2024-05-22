
aux_source_directory(. sources)
add_executable(KbCmd ${sources})
target_link_libraries(KbCmd PRIVATE common server entitydef network)
target_include_directories(KbCmd PRIVATE ../..)