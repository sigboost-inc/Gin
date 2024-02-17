cmake_minimum_required(VERSION 3.15)

project(Gin VERSION 1.0.0)

option(GIN_BUILD_EXAMPLES "Build the example app" OFF)

Include(FetchContent)

FetchContent_Declare(
    JUCE
    GIT_REPOSITORY https://github.com/sigboost-inc/JUCE.git
    GIT_TAG     origin/master_patched
)
FetchContent_MakeAvailable(JUCE)

add_subdirectory(modules)

if (GIN_BUILD_EXAMPLES)
    # TODO make target

    # set_property(GLOBAL PROPERTY USE_FOLDERS YES)
    # set(JUCE_ENABLE_MODULE_SOURCE_GROUPS ON CACHE BOOL "" FORCE)
    # set (CMAKE_CXX_STANDARD 20)
    # set (CMAKE_POSITION_INDEPENDENT_CODE ON)
    # set (CMAKE_OSX_DEPLOYMENT_TARGET 10.9)

    add_subdirectory(examples/Demo)
    add_subdirectory(examples/Effect)
    add_subdirectory(examples/Synth)
endif()
