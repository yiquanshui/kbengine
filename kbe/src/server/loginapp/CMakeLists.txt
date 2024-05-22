aux_source_directory(. sources)
add_library(LoginApp ${sources})
target_link_libraries(LoginApp PRIVATE server )
target_include_directories(LoginApp PRIVATE ..)
