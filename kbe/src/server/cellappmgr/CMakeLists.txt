
aux_source_directory(. sources)
add_library(CellAppManager ${sources})
target_link_libraries(CellAppManager PRIVATE helper server)
target_include_directories(CellAppManager PRIVATE ..)