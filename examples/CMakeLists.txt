add_library(xgboost IMPORTED OBJECT ${CMAKE_BINARY_DIR}/../dist/lib/libxgboost.a)
target_include_directories(xgboost INTERFACE ${CMAKE_BINARY_DIR}/../dist/include)

add_executable(hello_world hello_world.cpp)
target_link_libraries(hello_world PRIVATE xgboost)
