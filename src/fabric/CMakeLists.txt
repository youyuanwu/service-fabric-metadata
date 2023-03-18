

file(GLOB SOURCES
  include/*.h
  src/*.c
)

add_library(fabric_sdk STATIC
    ${SOURCES}
)

target_include_directories(fabric_sdk
  PUBLIC include
)