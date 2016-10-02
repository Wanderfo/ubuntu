# Compile and install opencv 2.4.9

## Download
Download and chose vision from this [page](https://sourceforge.net/projects/opencvlibrary/files/opencv-unix/2.4.9/) or direct [link](http://downloads.sourceforge.net/project/opencvlibrary/opencv-unix/2.4.9/opencv-2.4.9.zip?r=https%3A%2F%2Fsourceforge.net%2Fprojects%2Fopencvlibrary%2Ffiles%2Fopencv-unix%2F2.4.9%2F&ts=1475418484&use_mirror=nchc)

## Install
In opencv 3.1.0, there has a detailed introduction folder in doc/tutorials/introduction. 

### Required Package
```
sudo apt-get install build-essential
sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
sudo apt-get install python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev
```

### Compile
```
unzip opencv 
cd opencv    # change to where you download opencv
mkdir build
cd build
```

### Configuring
```
cmake -D CMAKE_BUILD_TYPE=Release -D CMAKE_INSTALL_PREFIX=/usr/local -D WITH_CUDA=OFF ..
make -j4  # runs 4 jobs in parallel
sudo make install
```
