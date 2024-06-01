add_subdirectory(src)
target_include_directories(${EXECUTABLE} PRIVATE inc)
target_include_directories(${EXECUTABLE} PRIVATE inc/api)
target_include_directories(${EXECUTABLE} PRIVATE inc/instances)
