---
layout: post
title: How to install ROS Kinetic
# summary: Markdown is a way to style text on the web. You control the display of the document; formating words as bold or italic, adding images, and creating lists are just a few of the things we can do with Markdown. Mostly, Markdown is just regular text with a few non-alphabetic characters thrown in.
# featured-img: how-to-install-ros-kinetic
# categories: ROS
featured-img: emile-perron-190221
categories: Guides
---

<!-- # How to install ROS Kinetic -->

<!-- [![My Video](https://img.youtube.com/vi/qP9JaVhnSS0/maxresdefault.jpg)](https://youtu.be/qP9JaVhnSS0?si=wY5DT3RtE8TeY69m) -->

<div style="text-align: center;">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/qP9JaVhnSS0?si=dZQY2t0PzN7XjXsj" frameborder="0" allowfullscreen></iframe>
</div>

## 1. Install Ubuntu 16.04 LTS

## 2. Setup source.list

```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```

## 3. Set up keys
If the key is newly added, you'll be able to verify the `imported` message on the terminal. On the other hand, if the key already exists, you'll see whether it has changed.

```
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
```

## 4. Update Ubuntu (Update Package index)
This command-line is recommended whenever you install Software or Package.
```
sudo apt-get update
```

## 5. Installation
There are three methods to install ROS, ranging from Desktop-Full install to ROS-Base. Among them, the Desktop-Full install is the recommended option. Additionally, to follow various tutorials on the web, using the recommended version is advised.

### 5.1 Desktop-Full Install (Recommended)
```
sudo apt-get install ros-kinetic-desktop-full
```

## 6. Initialize rosdep
`rosdep` is a command-line tool for installing system dependencies.
```
sudo rosdep init
rosdep update
```

## 7. Environment setup (option)
Now, environment variables will be set up whenever you open a new terminal. You can also edit them through `.bashrc`.
```
echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc source ~/.bashrc
```

### 7.1 Check whether Environment variables are well added.
If you can see environment variables like `ROS_ROOT` and `ROS_PACKAGE_PATH`, it means they have been added properly.
```
printenv | grep ROS
``` 

## 8. Dependencies for building packages
```
$ sudo apt install python-rosinstall python-rosinstall-generator python-wstool build-essential
```