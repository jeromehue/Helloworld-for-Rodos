cmake_minimum_required(VERSION 3.21)

project(
    SimpleApp
    VERSION 0.1.0
    DESCRIPTION "A test project for building an executable depending on an external library."
    HOMEPAGE_URL " "
    LANGUAGES CXX C ASM
)

add_executable(SimpleApp_Exe)
add_executable(SimpleApp::Exe ALIAS SimpleApp_Exe)

set_target_properties(SimpleApp_Exe PROPERTIES
    OUTPUT_NAME SimpleApp
    EXPORT_NAME Exe
)

add_subdirectory(source)

