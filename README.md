# face-landmark-localization
This is a project predict face landmarks (68 points).
- Model Size : 3.3MB.
- Speed : 5ms per face on i5-2.7GHz CPU.

## Install
- [caffe](https://github.com/BVLC/caffe)
- [dlib face detector](http://dlib.net/)
- add libdlib.a to your project lib path
- add face_lardmark.cpp to your caffe project example folder
- opencv<p>

## Usage

- CPP Demo : 
  Build dlib 下载源码并解压
  
  mkdir build
  
  cd build
  
  cmake ..
  
  make release=1
  
  添加Dlib文件夹到系统目录，
  修改CMakeList.txt中dlib的lib路径为自己的
  
  Build facelandmark
  
  cmake ..
  
  make 
  
  ./face_landmark
  
- Python Demo: python face_landmark.py (created by [jiangwqcooler](https://github.com/jiangwqcooler))

## notice
- This model was trained on dlib face detector. Other face detector may not get landmark result as good as dlib

## Result
![](result/7_result.jpg)
![](result/8_result.jpg)
