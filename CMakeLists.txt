
cmake_minimum_required (VERSION 2.6)

project (FaceAlgorithmDemo)

set(TensorRT_DIR /usr/local/TensorRT-8.6.1.6/)
# tensorrt 目录
# tensorrt path
if (CMAKE_SYSTEM_PROCESSOR MATCHES "aarch64")
    set(TensorRT_INCLUDE "/usr/include/aarch64-linux-gnu" CACHE INTERNAL "TensorRT Library include location")
    set(TensorRT_LIB "/usr/lib/aarch64-linux-gnu" CACHE INTERNAL "TensorRT Library lib location")
else()
    set(TensorRT_INCLUDE "{TensorRT_DIR}/include" CACHE INTERNAL "TensorRT Library include location")
    set(TensorRT_LIB "{TensorRT_DIR}/lib" CACHE INTERNAL "TensorRT Library lib location")
endif()

#添加子目录
add_subdirectory("FaceAlgorithm")
add_subdirectory("FaceAlgorithm_Test")

