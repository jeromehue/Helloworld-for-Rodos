target_sources(SimpleApp_Exe
    PRIVATE
        main.cpp
)

# Allow 32 bits packages to be found
unset(CMAKE_SIZEOF_VOID_P)
find_package(Rodos 0.1.0 REQUIRED)
target_link_libraries(SimpleApp_Exe PRIVATE Rodos::Rodos)
target_include_directories(SimpleApp_Exe PRIVATE /usr/local/include/rodos)

target_compile_features(SimpleApp_Exe PRIVATE cxx_std_17)
target_compile_options(SimpleApp_Exe PRIVATE -m32)
target_link_options(SimpleApp_Exe PRIVATE -m32)
