cmake_minimum_required(VERSION 3.15)

project(
    pbtest
    CSharp)

set(TARGET
    pbtest)

set(SOURCES
    ${CMAKE_CURRENT_SOURCE_DIR}/pbtest.cs)

add_executable(
    ${TARGET}
    ${SOURCES})

set_target_properties(${TARGET} PROPERTIES
    VS_DOTNET_TARGET_FRAMEWORK_VERSION "v4.7.2")

set_property(
    TARGET ${TARGET}
    PROPERTY VS_PACKAGE_REFERENCES
             "Google.Protobuf_3.22.1")
