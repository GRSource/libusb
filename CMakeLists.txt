
aux_source_directory(libusb LIBUSB_SOURCES)
aux_source_directory(libusb/os LIBUSB_SOURCES)


add_library(libusb STATIC ${LIBUSB_SOURCES})

#message("CMAKE_SOURCE_DIR : ${CMAKE_SOURCE_DIR}, ANDROID_ABI : ${ANDROID_ABI}")


