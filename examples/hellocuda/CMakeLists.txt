# Linking with CUDA

#Include the FindCUDA script
INCLUDE(FindCUDA)

#Set Include and Link directories
#INCLUDE_DIRECTORIES(${INCLUDEDIRS})

#SET(CUDA_NVCC_FLAGS ${CUDA_NVCC_FLAGS} ${CUDACOMPILEOPS})
CUDA_ADD_EXECUTABLE(hellcuda
  hellocuda.cu
  OPTIONS ${CUDACOMPILEOPS})

#If we needed to link any dynamic libraries
# We need to link against cryptopp
# TARGET_LINK_LIBRARIES(hellocuda ${LIBRARYDIRS})
