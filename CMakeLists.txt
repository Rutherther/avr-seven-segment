add_subdirectory(lib/avr-shift-registers)

add_avr_library(
        avr_seven_segment
        # sources
        src/seven-segment.c

        # headers
        include/seduce.h
)

avr_target_include_directories(avr_seven_segment ../include ../lib/avr-shift-registers/src)
avr_target_link_libraries(avr_seven_segment PUBLIC avr_shift_registers)