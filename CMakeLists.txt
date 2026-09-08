cmake_minimum_required(VERSION 3.22)
project(LabCore LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON)

set(LAB_ENGINE_DIR "$ENV{LAB_ENGINE_DIR}")
if(NOT LAB_ENGINE_DIR)
    set(LAB_ENGINE_DIR "C:/Users/jancz/Desktop/Lab")
endif()

include_directories(
    "${CMAKE_CURRENT_SOURCE_DIR}/include"
    "${LAB_ENGINE_DIR}/include"
    "${LAB_ENGINE_DIR}/src/glad/include"
    "${LAB_ENGINE_DIR}/external/lua"
    "${LAB_ENGINE_DIR}/build/_deps/glfw-src/include"
)

link_directories(
    "${LAB_ENGINE_DIR}/build/Release"
    "${LAB_ENGINE_DIR}/build/_deps/glfw-build/src/Release"
    "${LAB_ENGINE_DIR}/bin"
)

add_library(LabCore SHARED
    src/LabCore.cpp
    include/LabCore.h
    include/LabMath.h
    include/LabCamera.h
    include/LabFont.h
    include/LabDialogs.h
    include/LabExport.h
)

target_compile_definitions(LabCore PRIVATE GLAD_API_CALL_EXPORT)
if("LabCore" STREQUAL "LabCore")
    target_compile_definitions(LabCore PRIVATE LAB_CORE_BUILD)
endif()

if(MSVC)
    target_compile_options(LabCore PRIVATE /W4 /utf-8 /permissive-)
endif()

target_link_libraries(LabCore PUBLIC glfw3 glad gdi32 comdlg32)
