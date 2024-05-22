
find_package(OpenSSL REQUIRED)

aux_source_directory(. sources)
add_library(common STATIC ${sources})

target_include_directories(common PUBLIC . ..)
target_link_libraries(common PUBLIC fmt xml helper INTERFACE utf8lib PRIVATE ${OPENSSL_LIBRARIES})
target_compile_options(common PUBLIC -Wno-deprecated-declarations)