Follow this tutorial for Ubuntu Linux:
https://docs.ros.org/en/foxy/Installation/Ubuntu-Install-Debians.html


In short these are the commands you need to enter: 
```
locale  # check for UTF-8

sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8

locale  # verify settings

apt-cache policy | grep universe

sudo apt install software-properties-common
sudo add-apt-repository universe


sudo apt update && sudo apt install curl gnupg2 lsb-release
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key  -o /usr/share/keyrings/ros-archive-keyring.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null

sudo apt update

sudo apt upgrade

sudo apt install ros-foxy-desktop

source /opt/ros/foxy/setup.bash
```

Or simply run the bash script I found here (https://github.com/Tiryoh/ros2_setup_scripts_ubuntu/blob/master/ros2-foxy-desktop-main.sh)

Run instructions:

Go to dir in terminal and enter:
```
chmod +x ros2-foxy-desktop-main.sh
./ros2-foxy-desktop-main.sh
```
