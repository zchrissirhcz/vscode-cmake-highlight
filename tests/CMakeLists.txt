# VERSION
cmake_minimum_required(VERSION 3.20)
project(digimon)

# CMAKE_EXPORT_COMPILE_COMMANDS
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_POSITION_INDEPENDENT_CODE ON)

# CMAKE_C_STANDARD
set(CMAKE_C_STANDARD 99)

# CMAKE_CXX_STANDARD
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_POSITION_INDEPENDENT_CODE ON)

add_link_options(-fopenmp)

add_library(hello hello.cpp)
target_link_options(hello PUBLIC -fopenmp)

# SET
cmake_policy(SET CMP0057 NEW)

# STATUS
message(STATUS "APP/D: ${ARGN}")

# FATAL_ERROR
message(FATAL_ERROR "APP/E: ${ARGN}")

# READ
# CONTENT
file(READ ${DISTRO_FILE} CONTENT)

# PARENT_SCOPE
set(${OUTPUT_VAR} PARENT_SCOPE)

# SORT
list(SORT APP_ARCH)

# COMMAND, WORKING_DIRECTORY, OUTPUT_VARIABLE, RESULT_VARIABLE
execute_process(
    COMMAND ${GIT_EXECUTABLE} rev-parse ${extra_git_args} HEAD
    WORKING_DIRECTORY "${SOURCE_DIR}"
    OUTPUT_VARIABLE REVISION
    RESULT_VARIABLE RET
)

# The doc word should not always being considered as highlighted keyword:
mysdk_define(
  my_xxx
  LIBRARY my_xxx
  INCS inc/*.h
  VERSION_FILE src/version.c
  SAMPLE_CODE samplecode
  RELEASE_NOTES releasenotes.txt
  DOCS doc/*.pdf   # this `doc`
)

# The word and should not always be highlighted:
neon_sim_add_test(and)
