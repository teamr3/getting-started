# Install librealsense SDK 2.0 using source builds

https://github.com/IntelRealSense/librealsense/blob/master/doc/installation.md

```
sudo apt-get update && sudo apt-get upgrade && sudo apt-get dist-upgrade
git clone https://github.com/IntelRealSense/librealsense.git
```

```
cd librealsense
sudo apt-get install git libssl-dev libusb-1.0-0-dev libudev-dev pkg-config libgtk-3-dev
sudo apt-get install libglfw3-dev libgl1-mesa-dev libglu1-mesa-dev
```

```
./scripts/setup_udev_rules.sh
./scripts/patch-ubuntu-kernel-4.16.sh

echo 'hid_sensor_custom' | sudo tee -a /etc/modules
```

```
sudo add-apt-repository ppa:ubuntu-toolchain-r/test
sudo apt-get update
```

Non-CUDA CMake Flags

```
cmake ../ -DFORCE_RSUSB_BACKEND=ON -DCMAKE_BUILD_TYPE=release -DBUILD_EXAMPLES=true -DBUILD_GRAPHICAL_EXAMPLES=true -DBUILD_PYTHON_BINDINGS:bool=true -DBUILD_CV_EXAMPLES:bool=true 

sudo make uninstall && make clean && make && sudo make install
```



# Install ros2 wrapper for realsense

https://github.com/IntelRealSense/realsense-ros/tree/ros2


# Install realsense-gstreamer (Not Recommended)

instructions go here


# Cuda install for sdk (has issues in 20.04):
<p>
add `-DBUILD_WITH_CUDA:bool=true` at the end
</p>