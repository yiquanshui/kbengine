
find_package(tinyxml CONFIG REQUIRED)
add_library(xml xml.cpp)
target_link_libraries(xml PUBLIC helper
		unofficial-tinyxml::unofficial-tinyxml
)

target_include_directories(xml PUBLIC . PRIVATE ..)