cmake_minimum_required(VERSION 3.12)
project(websockify-c)

# Look for OpenSSL
find_package(OpenSSL REQUIRED)

add_executable(websockify websocket.c websockify.c)

target_link_libraries(websockify PRIVATE OpenSSL::SSL)

install(TARGETS websockify DESTINATION bin)
