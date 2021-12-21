target_sources(SimpleApp_Exe
    PRIVATE
        main.cpp
)

find_package(Rodos-stm32f4 0.1.0 REQUIRED)
target_link_libraries(SimpleApp_Exe PRIVATE Rodos::Rodos)
