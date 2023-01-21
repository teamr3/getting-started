## How to build opencv from source with backend features enabled
#### Note: This process takes about 2 hours so sit back, grab a mimosa and put on a movie.

Ref link:  https://qiita.com/asahi0301/items/3c287190348552f19415 </br>
Move the `swap` and `cv2_install` files to a dir of your choice </br>

Run this to enable running bash files
```
chmod +x swap.sh
chmod +x cv2_install.sh
```

Run this to allocate memory and avoid memory errors and then build opencv from source
```
sh swap.sh
sh cv2_install.sh opencv
```
or use this after installing (`sudo apt-get install dos2unix`)

```
dos2unix cv2_install.sh
```
and then:
```
./swap.sh
./cv2_install.sh opencv
```

After you start install, just say yes or A for all wherever necessary and keep an eye from time to time. if you run into errors contact @tanmayyb

The configurations in the file
```
-D WITH_CUDA=ON \
    -D CUDA_ARCH_BIN="5.3" \
    -D CUDA_ARCH_PTX="" \
    -D OPENCV_EXTRA_MODULES_PATH=../../opencv_contrib-4.1.0/modules \
    -D WITH_GTK=ON \
    -D WITH_GTK_X_2=ON \
    -D WITH_OPENGL=ON \
    -D WITH_GSTREAMER=ON \
    -D WITH_LIBV4L=ON \
    -D BUILD_opencv_python2=ON \
    -D BUILD_opencv_python3=ON \
    -D BUILD_TESTS=OFF \
    -D BUILD_PERF_TESTS=OFF \
    -D BUILD_EXAMPLES=OFF \
    -D CMAKE_BUILD_TYPE=RELEASE \
    -D CMAKE_INSTALL_PREFIX=/usr/local ..
```
Gstreamer, extramodulespath, GTK should be on.
