cmake_minimum_required(VERSION 3.12)

if(NOT IS_CPPM_LOADED)
include(cmake/cppm_tool.cmake)
endif()
cppm_project()
project(test-shared VERSION 0.0.1 LANGUAGES C CXX)
cppm_setting()

cppm_cxx_standard(17)
cppm_compiler_option(DEFAULT)



cppm_target_define(test-shared SHARED  
SOURCES 
	src/test.cpp)


cppm_target_dependencies(test-shared 
)

cppm_target_install(test-shared)

