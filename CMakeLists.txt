cmake_minimum_required(VERSION 2.8.8)


add_subdirectory( googletest )

SET(CMAKE_CXX_STANDARD 11)

ADD_EXECUTABLE(test
    unit_test.cpp
)

ADD_EXECUTABLE(exp
    expFactory.cpp
    main2.cpp
)

TARGET_LINK_LIBRARIES(test gtest)
TARGET_COMPILE_DEFINITIONS(test PRIVATE gtest_disable_pthreads=ON)
