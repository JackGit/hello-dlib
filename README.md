This is demo of QT + opencv + Dlib

### environment

windows 10 (64bit), QT 5.8.0 (mingw 32bit), dlib 19.2, opencv 2.4.13

### build opencv for mingw

refer https://github.com/JackGit/hello-opencv/blob/master/README.md

### build dlib for mingw

1. download [dlib-19.2](http://dlib.net/files/dlib-19.2.zip), and extract to `D:\dlib-19.2`

2. download [cmake-gui](https://cmake.org/files/v3.7/cmake-3.7.2-win64-x64.msi) for win64 and install it

3. make sure you have `D:\Qt\Qt5.8.0\Tools\mingw530_32\bin` in your windows environment path, this is required when you make file for mingw in cmake

4. open cmake-gui, select `D:\dlib-19.2\dlib` as source code, create a directory, which I created `D:\dlib-19.2\build`, as build directory

5. click CMake Configure button

6. then click CMake Generate button

7. open terminal under `D:\dlib-19.2\build`, execute `mingw32-make`, this takes 10 mins in my machine

8. rename `D:\dlib-19.2\build` into `D:\dlib-19.2\lib`

9. create folder `D:\dlib-19.2\include` and move `D:\dlib-19.2\dlib` into it

10. done

You now have directory like:

![dlib directory](http://ofkyhrvda.bkt.clouddn.com/post/image/dlib_directory_structure.png)

### landmarks.dat

download file and put it somewhere: http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2

### QT

config .pro file and write demo code as in this repository, then you are ready to go

### screenshot

![screenshot](http://ofkyhrvda.bkt.clouddn.com/post/image/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20170214115809.png)

### references

[Dlib (C++) install on PC with MingW and QT environment(part 1)](https://www.youtube.com/watch?v=qC2U0-SAasU)

[Dlib (C++) install on PC with MingW and QT environment(part 2)](https://www.youtube.com/watch?v=wg5g5bQMNbA)
