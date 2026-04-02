cmake_minimum_required(VERSION 3.24)
project(ImGuiColorTextEdit LANGUAGES CXX)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

file(GLOB IMGUI_TEXT_EDIT_SOURCES
  TextEditor.cpp
)

add_library(ImGuiColorTextEdit STATIC ${IMGUI_TEXT_EDIT_SOURCES})
target_include_directories(ImGuiColorTextEdit PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_SOURCE_DIR}/3rdparty/imgui
)
