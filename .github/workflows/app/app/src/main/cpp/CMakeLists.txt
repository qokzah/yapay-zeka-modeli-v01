cmake_minimum_required(VERSION 3.22.1)
project("offlineai")

set(CMAKE_CXX_STANDARD 17)

# llama.cpp kaynak dosyaları
add_library(
    llama-android
    SHARED
    native-lib.cpp
)

find_library(
    log-lib
    log
)

target_link_libraries(
    llama-android
    ${log-lib}
)
