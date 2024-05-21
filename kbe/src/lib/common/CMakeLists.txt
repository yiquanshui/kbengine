
aux_source_directory(. sources)
add_library(common STATIC ${sources})
set(includes
		"../dependencies"
		"..")
target_include_directories(common PUBLIC ${includes} PRIVATE .)
target_link_libraries(common PUBLIC fmt)
target_compile_options(common PUBLIC -Wno-deprecated-declarations)