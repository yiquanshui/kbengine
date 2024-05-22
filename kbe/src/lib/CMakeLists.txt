
add_subdirectory(dependencies)
add_subdirectory(xml)
add_subdirectory(common)

#aux_source_directory(common CommonSources)
#add_library(kbe
#		${CommonSources}
#)
#
#target_include_directories(kbe PUBLIC . PRIVATE common)
#
#target_link_libraries(kbe PUBLIC fmt utf8lib)

add_subdirectory(math)
add_subdirectory(helper)
add_subdirectory(pyscript)
add_subdirectory(server)
add_subdirectory(entitydef)
add_subdirectory(resmgr)
add_subdirectory(network)
add_subdirectory(thread)
add_subdirectory(navigation)
add_subdirectory(db_interface)