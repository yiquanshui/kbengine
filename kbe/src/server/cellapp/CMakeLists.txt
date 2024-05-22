
aux_source_directory(. sources)
add_executable(CellApp ${sources})

#find_package(tmxparser COMPONENTS tmxparser)
target_link_libraries(CellApp PRIVATE common network helper pyscript entitydef Navigation)
target_include_directories(CellApp PRIVATE ..)