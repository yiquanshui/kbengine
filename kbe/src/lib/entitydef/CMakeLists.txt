
aux_source_directory(. sources)
#find_package(tinyxml CONFIG REQUIRED)

add_library(entitydef ${sources})
#target_link_libraries(entitydef PUBLIC common pyscript PRIVATE unofficial-tinyxml::unofficial-tinyxml)
target_link_libraries(entitydef PUBLIC common pyscript PRIVATE network)

