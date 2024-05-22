
add_executable(baseapp)
#file(GLOB sources CONFIGURE_DEPENDS *.cpp *.h)
#find_package(Python3 COMPONENTS Development)
aux_source_directory(. sources)
target_sources(baseapp PRIVATE ${sources})
target_link_libraries(baseapp PUBLIC common pyscript server helper entitydef PRIVATE network)

target_include_directories(baseapp PRIVATE ..)