add_subdirectory(bsp)

target_sources_ifdef(CONFIG_SERIAL ${EXECUTABLE} PRIVATE r_sci_uart/r_sci_uart.c)