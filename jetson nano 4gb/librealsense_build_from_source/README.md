# Install librealsense using source builds
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


```
cmake ../-DFORCE_RSUSB_BACKEND=ON -DBUILD_PYTHON_BINDINGS:bool=true -DPYTHON_EXECUTABLE=... -DCMAKE_BUILD_TYPE=release -DBUILD_EXAMPLES=true -DBUILD_GRAPHICAL_EXAMPLES=true -DBUILD_WITH_CUDA:bool=true

sudo make uninstall && make clean && make && sudo make install
```

