cmake_minimum_required(VERSION 3.0.0)
project(doc_demo VERSION 0.1.0)

# Add the cmake folder so the FindSphinx module is found
set(CMAKE_MODULE_PATH "${PROJECT_SOURCE_DIR}/cmake" ${CMAKE_MODULE_PATH})

include(CTest)
enable_testing()

add_subdirectory(selva)
add_subdirectory(docs)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
