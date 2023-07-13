cmake_minimum_required(VERSION 3.22)

project(study_cmake_multitarget_os)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/build/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/build/lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/build/bin)


add_executable(study_cmake_multitarget_os ${CMAKE_CURRENT_SOURCE_DIR}/src/main.cpp)

if(UNIX)
	target_link_libraries(study_cmake_multitarget_os
		PRIVATE
		-lstdc++
	)
endif(UNIX)
