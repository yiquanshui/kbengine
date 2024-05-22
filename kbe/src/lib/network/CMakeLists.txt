
find_package(CURL REQUIRED)
aux_source_directory(. sources)
add_library(network ${sources})
target_compile_definitions(network PUBLIC HAS_EPOLL)
target_include_directories(network PUBLIC .)
target_link_libraries(network PRIVATE common thread ${CURL_LIBRARIES})