add_executable(myunittest
  lib_test.cpp
)

target_link_libraries(myunittest PRIVATE
    mylib
    gtest_main
)