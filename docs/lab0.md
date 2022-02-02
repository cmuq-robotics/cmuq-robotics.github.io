---
layout: default
title: Lab0: Preparation
---

# Installation of the ROS environment for robot control and simulation

In this course, we will work with Ubuntu 18.04 and ROS Melodic Morenia. We highly recommend you to use
VMware and the provided virtual machine image that already contains a preinstalled environment with the
following software:

- Ubuntu 18.04
- ROS Melodic Morenia
- Catkin Command Line Tools
- Terminator
- Git
- Sublime Text

## Install VMware

To run the provided virtual machine you need the **VMware Workstation 15 Pro (Windows, Linux)** or **VMware
Fusion 11 (macOS)**. This software can be installed on the VMware Campus Webstore (free for students):
https://www.cmu.edu/computing/software/all/vmware/index.html, and fill in the form to request an academic license.
Follow the given instructions to download and install the software from VMware. We recommend that
you have at least 20GB of available disk space on your computer to run the virtual machine.

## Download Image with Ubuntu+ROS

Download the zipped folder [Ubuntu_18_04_ROS.zip (~6.18 GB)](https://drive.google.com/file/d/1aDhigSu-y4BNaHdC2mVcUiJMYaZkWzaM/view?usp=sharing) from Google Drive and extract it. If you
extract the zipped folder in an Ubuntu distribution, make sure that you use `p7zip`, that you can install with:

.. code-block:: bash
   sudo apt-get install p7zip-full

If you have issues unzipping the file on macOS, use the command line tool ditto

.. code-block:: bash
   ditto -xk <zip file> <target_dir>
