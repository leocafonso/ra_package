target_include_directories(${EXECUTABLE} PRIVATE cmsis/Device/RENESAS/Include)
target_include_directories(${EXECUTABLE} PRIVATE mcu/all)

#source directories
file(GLOB_RECURSE bsp_files 
"${CMAKE_CURRENT_SOURCE_DIR}/mcu/all/*.c"
"${CMAKE_CURRENT_SOURCE_DIR}/cmsis/Device/RENESAS/Source/*.c")

set(srcs ${bsp_files})

target_sources(${EXECUTABLE} PRIVATE ${srcs})

message(${CONFIG_SOC_SERIES})
target_include_directories(${EXECUTABLE} PRIVATE mcu/${CONFIG_SOC_SERIES})
