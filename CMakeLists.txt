cmake_minimum_required( VERSION 2.8 )
project( stereo_calib )

# 添加c++ 11标准支持
set( CMAKE_CXX_FLAGS "-std=c++11" )
set(OpenCV_DIR "/home/megvii/SLAM_project/tools/opencv-3.4.1/build")
# 寻找OpenCV库
find_package( OpenCV REQUIRED)
# 添加头文件
include_directories( ${OpenCV_INCLUDE_DIRS} )

#add_executable( stereo_calib main.cpp )
#add_executable(calibration calibration.cpp)
add_executable(stereo_calib stereo_calib.cpp)
# 链接OpenCV库
#target_link_libraries( stereo_calib ${OpenCV_LIBS} )
#target_link_libraries( calibration ${OpenCV_LIBS} )
target_link_libraries( stereo_calib ${OpenCV_LIBS} )
