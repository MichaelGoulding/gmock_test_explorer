file(GLOB src_files CONFIGURE_DEPENDS
    *.cpp
    *.h
)

add_executable(QEngClientUnitTests
    ${src_files}
)

target_link_libraries(QEngClientUnitTests PRIVATE
    GTest::gtest
    #GTest::gmock
    #GTest::gmock_main
    GTest::gtest_main
)

gtest_discover_tests(QEngClientUnitTests)
