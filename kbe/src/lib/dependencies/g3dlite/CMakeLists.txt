
aux_source_directory(. Sources)
add_library(G3dLite ${Sources})
target_include_directories(G3dLite PUBLIC .)