
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
target_include_directories(sigar INTERFACE . PRIVATE
		/usr/include/tirpc
)
