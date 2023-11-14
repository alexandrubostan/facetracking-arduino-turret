cmake_minimum_required(VERSION 3.20)

project(facerec)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_INSTALL_PREFIX ${CMAKE_SOURCE_DIR})
set(CMAKE_BUILD_TYPE Release)

include_directories(include)
add_executable(${PROJECT_NAME}
	src/facerec.cpp
	src/serial.cpp
)

target_compile_options(${PROJECT_NAME} PRIVATE -Wall)
install(TARGETS ${PROJECT_NAME} DESTINATION bin)

find_package(OpenCV REQUIRED)
target_link_libraries(${PROJECT_NAME} ${OpenCV_LIBS})
