cmake_minimum_required(VERSION 3.11)

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

set_property(
    TARGET ${TARGET}
    PROPERTY VS_PACKAGE_REFERENCES
             "Google.Protobuf_3.25.1")
