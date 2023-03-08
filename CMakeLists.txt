


cmake_minimum_required(VERSION 3.4.1)

set(${CMAKE_C_FLAGS}, "${CMAKE_C_FLAGS}")

# now build app's shared lib
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=gnu++17")


AUX_SOURCE_DIRECTORY(${CMAKE_CURRENT_SOURCE_DIR}/libusb LIBUSB_SOURCES)
AUX_SOURCE_DIRECTORY(${CMAKE_CURRENT_SOURCE_DIR}/libusb/os LIBUSB_SOURCES)

set(LIBUSB_INCLUDE_DIR
        ${CMAKE_CURRENT_SOURCE_DIR}/android
        ${CMAKE_CURRENT_SOURCE_DIR}/libusb
        ${CMAKE_CURRENT_SOURCE_DIR}/libusb/os
        CACHE INTERNAL "libusb include dir"
)


add_library(libusb STATIC ${LIBUSB_SOURCES})

#message("CMAKE_SOURCE_DIR : ${CMAKE_SOURCE_DIR}, ANDROID_ABI : ${ANDROID_ABI}")


