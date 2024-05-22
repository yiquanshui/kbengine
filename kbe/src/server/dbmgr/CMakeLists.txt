aux_source_directory(. sources)
add_library(DbManager ${sources})
target_link_libraries(DbManager PUBLIC DbInterface common pyscript)
target_include_directories(DbManager PRIVATE ..)
