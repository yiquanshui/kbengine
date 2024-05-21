
set(sources
		sigar.c
		sigar_cache.c
		sigar_fileinfo.c
		sigar_format.c
		sigar_getline.c
		sigar_ptql.c
		sigar_util.c
		linux_sigar.c
)

add_library(sigar ${sources})
find_package(PkgConfig QUIET)
pkg_check_modules(PC_TIRPC libtirpc)
find_path(TIRPC_INCLUDE_DIRS
		NAMES netconfig.h
		PATH_SUFFIXES tirpc
		HINTS ${PC_TIRPC_INCLUDE_DIRS}
)

find_library(TIRPC_LIBRARIES
		NAMES tirpc
		HINTS ${PC_TIRPC_LIBRARY_DIRS}
)

set(TIRPC_VERSION ${PC_TIRPC_VERSION})

include(FindPackageHandleStandardArgs)

find_package_handle_standard_args(TIRPC
		REQUIRED_VARS TIRPC_LIBRARIES TIRPC_INCLUDE_DIRS
		VERSION_VAR TIRPC_VERSION
)

mark_as_advanced(TIRPC_INCLUDE_DIRS TIRPC_LIBRARIES)
target_include_directories(sigar INTERFACE . PRIVATE ${TIRPC_INCLUDE_DIRS})
#target_include_directories(sigar INTERFACE . PRIVATE
#		/usr/include/tirpc
#)

target_link_libraries(sigar PUBLIC ${TIRPC_LIBRARIES})
