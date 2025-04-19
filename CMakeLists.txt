cmake_minimum_required(VERSION 3.22)

project(TestApp VERSION 0.1 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Qt6 REQUIRED COMPONENTS Quick Test Qml Gui)

qt_standard_project_setup()

qt_add_executable(TestApp
    src/main.cpp
)

qt_add_qml_module(TestApp
    URI testapp
    VERSION 1.0
    QML_FILES
        qml/Main.qml
)

set_target_properties(TestApp PROPERTIES
    MACOSX_BUNDLE FALSE
    WIN32_EXECUTABLE FALSE
)

target_link_libraries(TestApp PRIVATE
    Qt6::Quick
)

enable_testing()

add_subdirectory(tests/cpp-tests)
add_subdirectory(tests/qt-tests)
add_subdirectory(tests/qml-tests)

add_library(DummyIOS STATIC src/hello_ios.cpp)
add_library(CodeQLTarget STATIC src/dummy_codeql.cpp)
