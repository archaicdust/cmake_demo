include_directories(${PROJECT_SOURCE_DIR}/lib)
set(APP_SRC main.c)
add_executable(main ${APP_SRC})

link_directories(${PROJECT_BINARY_DIR}/lib)
target_link_libraries(main hello)

message("CMAKE_SOURCE_DIR= ${CMAKE_SOURCE_DIR}")
message("CMAKE_BINARY_DIR= ${CMAKE_BINARY_DIR}")
