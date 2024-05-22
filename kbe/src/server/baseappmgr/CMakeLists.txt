
aux_source_directory(. sources)
add_executable(BaseAppManager ${sources})
target_link_libraries(BaseAppManager PRIVATE server network)
#target_link_libraries(baseapp PUBLIC common pyscript server helper entitydef PRIVATE network)
target_include_directories(BaseAppManager PRIVATE ..)
