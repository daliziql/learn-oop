CMAKE_MINIMUM_REQUIRED(VERSION 3.9)
PROJECT(example4)

AUX_SOURCE_DIRECTORY(${CMAKE_CURRENT_SOURCE_DIR} SRC_LIST)

SET(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/bin)

ADD_EXECUTABLE(${PROJECT_NAME} ${SRC_LIST})

SET_TARGET_PROPERTIES(${PROJECT_NAME}
        PROPERTIES
        CXX_STANDARD 14
        CXX_EXTENSIONS OFF
        CXX_STANDARD_REQUIRED ON
        POSITION_INDEPENDENT_CODE 1
        )