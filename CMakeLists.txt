cmake_minimum_required(VERSION 3.5)

set(PROJECT_NAME HandDetectionCV)

project(${PROJECT_NAME})

find_package(OpenCV REQUIRED)

file(GLOB_RECURSE SOURCES src/*.cpp src/*.h  src/*.c)

add_executable(${PROJECT_NAME} ${SOURCES})

include_directories(
	${OpenCV_INCLUDE_DIRS}
        "./src"
    )

target_link_libraries(${PROJECT_NAME} ${OpenCV_LIBS})
