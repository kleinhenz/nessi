
# ~~ cntr_hdf5 shared library

set(cntr_hdf5_src hdf5_interface.cpp)
add_library(cntr_hdf5 SHARED ${cntr_hdf5_src})
target_link_libraries(cntr_hdf5 PUBLIC hdf5::base ${COMMON_LIBS})
target_compile_definitions(cntr_hdf5 PUBLIC "-DCNTR_USE_HDF5")
install(TARGETS cntr_hdf5 EXPORT nessi-config DESTINATION lib)
