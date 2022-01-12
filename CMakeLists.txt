cmake_minimum_required(VERSION 3.14)

project(libffi-boilerplate)

SET(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -static")

include_directories("${libffi_ROOT}/include")

add_executable(${PROJECT_NAME}
    "src/main.cpp"
)

target_link_libraries(${PROJECT_NAME} "${libffi_ROOT}/lib/libffi.a")