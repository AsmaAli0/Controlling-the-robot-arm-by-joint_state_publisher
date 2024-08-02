# Controlling-the-robot-arm-by-joint_state_publisher
# ROS Workspace Setup (Catkin)

This guide provides step-by-step instructions to set up a ROS workspace using Catkin.

## Prerequisites

- *Ubuntu*: Ensure you are using Ubuntu 20.04 or another compatible version.
- *ROS*: Ensure ROS (e.g., Noetic) is already installed

  currently we are working on the home directory
  ## lets start withe first command
  for creating a new workspace then entering a new folder
```
mkdir catkin_ws
```

```
cd catkin_ws
```

now we create a source 
```
mkdir src
```

while we are inside the catkin_ws folder we start to compile by running the command :
```
catkin_make
```

![11](https://github.com/user-attachments/assets/7d1218d6-edc5-4200-b62e-0aac9f5784a5)
now we have two folders under the command ```ls```
![22](https://github.com/user-attachments/assets/70fc6bad-c4d9-41e8-8141-28602dcd5998)



###  Source the Setup File

Navigate to the devel directory and list its contents:


```
cd devel/
```
```
ls
```

*Explanation:*
- cd devel/ changes the current directory to devel, the development space where Catkin places built products and environment setup files.
- ls lists the contents of the devel directory. You should see various setup scripts.



This command runs the setup.bash script, which sets up the environment for using the ROS packages built in the workspace. It configures environment variables needed by ROS tools and packages.

###  Update Bash Configuration

Edit your .bashrc file to include the setup script, ensuring the environment is set up every time you open a new terminal:

![333](https://github.com/user-attachments/assets/9db909aa-aa5c-4526-a613-14c6928a3b35)




## after finishing the workspace lets get to the installation
##  Add the “arduino_robot_arm” package to “src” folder ```cd src``` then copy this command :
```
sudo apt install git
```
![333](https://github.com/user-attachments/assets/9db909aa-aa5c-4526-a613-14c6928a3b35)
- ```git clone https://github.com/smart-methods/arduino_robot_arm```
- now go back to the (catkin_ws) using command ```cd ..``` ,then

```
rosdep install --from-paths src --ignore-src -r -y
```
- run the command ```sudo apt-get install ros-noetic-moveit```

<img width="955" alt="44" src="https://github.com/user-attachments/assets/53622139-00cf-41da-8cf3-701d591c8edc">
run the command 
```
sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
```

```
sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
```

```
sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
```

compile the package

```
catkin_make
```

![55](https://github.com/user-attachments/assets/7f0bbdee-2a00-4da8-b3cf-8b1f4b4335a0)


## The arm will appear after the previous command in the picture  on another window
![Screenshot 2024-08-02 143758](https://github.com/user-attachments/assets/51bc65aa-1660-45b3-b4c6-fdd853c3cdea)
