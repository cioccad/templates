# SPDX-License-Identifier: BSD-3-Clause

cmake_minimum_required(VERSION 3.14)

set(PROJECT_NAME "Project-Template")
set(PROJECT_DESCRIPTION "This is my template project")
set(PROJECT_VERSION 1.0)
set(PROJECT_TARGET "output")

project(${PROJECT_NAME} VERSION ${PROJECT_VERSION}
        DESCRIPTION ${PROJECT_DESCRIPTION}
        LANGUAGES CXX C ASM)

add_compile_options(-Wall -Wextra -pedantic)

add_executable(${PROJECT_TARGET}
               main.cc)

target_compile_features(${PROJECT_TARGET}
                        PUBLIC cxx_std_14)

set_target_properties(${PROJECT_TARGET}
                      PROPERTIES CXX_EXTENSIONS OFF)
