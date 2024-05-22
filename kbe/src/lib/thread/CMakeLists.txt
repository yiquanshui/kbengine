
add_library(thread threadpool.cpp concurrency.cpp)
target_include_directories(thread PUBLIC .)
target_link_libraries(thread PRIVATE common)