cmake_minimum_required(VERSION 2.8)

include_directories(include)
  
project(Jasper C)

file(GLOB jasper_base_sources "base/*.c")
file(GLOB jasper_jp2_sources "jp2/*.c")
file(GLOB jasper_jp2_headers "jp2/*.h")
file(GLOB jasper_jpc_sources "jpc/*.c")
file(GLOB jasper_jpc_headers "jpc/*.h")
file(GLOB jasper_headers "include/jasper/*.h")
add_library(jasper STATIC ${jasper_base_sources} ${jasper_headers}
  ${jasper_jp2_sources} ${jasper_jp2_headers}
  ${jasper_jpc_sources} ${jasper_jpc_headers})
set_target_properties(jasper PROPERTIES COMPILE_FLAGS "-fPIC -Wall -Wformat-security -fstack-protector -g -O2 -march=native -ftree-vectorize")
