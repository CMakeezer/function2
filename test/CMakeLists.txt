add_executable(function2_tests
        ${CMAKE_CURRENT_LIST_DIR}/../include/function2/function2.hpp
        ${CMAKE_CURRENT_LIST_DIR}/assign-and-constructible-test.cpp
        ${CMAKE_CURRENT_LIST_DIR}/build-test.cpp
        ${CMAKE_CURRENT_LIST_DIR}/empty-function-call-test.cpp
        ${CMAKE_CURRENT_LIST_DIR}/function2-test.hpp
        ${CMAKE_CURRENT_LIST_DIR}/functionality-test.cpp
        ${CMAKE_CURRENT_LIST_DIR}/noexcept-test.cpp
        ${CMAKE_CURRENT_LIST_DIR}/self-containing-test.cpp
        ${CMAKE_CURRENT_LIST_DIR}/standard-compliant-test.cpp
        ${CMAKE_CURRENT_LIST_DIR}/type-test.cpp
        ${CMAKE_CURRENT_LIST_DIR}/multi-signature-test.cpp
        ${CMAKE_CURRENT_LIST_DIR}/regressions.cpp
        ${CMAKE_CURRENT_LIST_DIR}/view-test.cpp
        ${CMAKE_CURRENT_LIST_DIR}/overload-test.cpp)

target_link_libraries(function2_tests
        PRIVATE
        function2
        GTest::GTest
        GTest::Main)

add_test(NAME function2-unit-tests COMMAND function2_tests)

add_executable(function2_playground
        ${CMAKE_CURRENT_LIST_DIR}/../include/function2/function2.hpp
        ${CMAKE_CURRENT_LIST_DIR}/playground.cpp)

target_link_libraries(function2_playground
        PRIVATE
        function2)
