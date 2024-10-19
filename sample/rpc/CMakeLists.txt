set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -DSTATICLIB")

file(GLOB SRC_LIST "*.cpp")
file(GLOB HEADERS "*.h")

add_executable(rpc rpc.cpp)
target_link_libraries(rpc PUBLIC ${BCOS_C_SDK_STATIC_TARGET})
