find_package(Silo)

if(Silo_FOUND AND WITH_CPP14 AND NOT WITH_CUDA)
  add_executable(sph main.cpp kernels.c)
  include_directories(${Silo_INCLUDE_DIR})
  target_link_libraries(sph ${Silo_LIBRARY})
endif()
