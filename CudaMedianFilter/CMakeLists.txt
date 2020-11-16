cmake_minimum_required(VERSION 3.16)
project(CudaMedianFilter CUDA)

set(CMAKE_CUDA_STANDARD 14)

add_executable(CudaMedianFilter main.cpp medianFilter.cu stuff.h
        EasyBMP/EasyBMP.h EasyBMP/EasyBMP_DataStructures.h EasyBMP/EasyBMP_VariousBMPutilities.h
        EasyBMP/EasyBMP_BMP.h EasyBMP/EasyBMP.cpp)

set_target_properties(
        CudaMedianFilter
        PROPERTIES
        CUDA_SEPARABLE_COMPILATION ON)