
set(sources
		debug_helper.cpp
		debug_option.cpp
		eventhistory_stats.cpp
		profile.cpp
		profiler.cpp
		profile_handler.cpp
		script_loglevel.cpp
		sys_info.cpp
		watch_pools.cpp
		watcher.cpp
)

find_package(log4cxx)
#find_package(tinyxml CONFIG REQUIRED)
add_library(helper STATIC ${sources})
target_include_directories(helper PUBLIC . PRIVATE ..
		$<TARGET_PROPERTY:log4cxx,INTERFACE_INCLUDE_DIRECTORIES>
)
target_link_libraries(helper PUBLIC common log4cxx sigar resmgr
)
