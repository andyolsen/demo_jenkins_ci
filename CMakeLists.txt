cmake_minimum_required(VERSION 3.28)

project(MyProject)

add_executable(app src/main.cc)

enable_testing()
add_executable(test_app tests/test_main.cc)
add_test(NAME run_tests COMMAND test_app)
