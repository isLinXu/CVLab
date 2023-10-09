cmake_minimum_required(VERSION 3.24)
project(cv_dl_lab)

set(CMAKE_CXX_STANDARD 17)

set(TARGET_LIBS "/usr/local/include/opencv4/")
find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )
set(OpenCV_LIBS opencv_core opencv_imgproc opencv_highgui opencv_imgcodecs opencv_features2d opencv_photo opencv_video opencv_objdetect)



add_executable(cv_dl_lab main.cpp)

#目标链接库
target_link_libraries(cv_dl_lab
        ${OpenCV_LIBS}
        ${CMAKE_THREAD_LIBS_INIT}
        )



