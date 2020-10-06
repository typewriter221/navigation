# Autonomous Navigation with Mobile Robots using Deep Learning and the Robot Operating System	


# System and softwares information 

Ubuntu 16.04/18.04

ROS Kinetic/Medolic

Gazebo 7/8


# How to load these world files.

- First, download the 3D models, then extract and copy them to your Gazebo folder located at /home/<use_name>/.gazebo/models

- Second, copy world files inside world_files folder into your project folder where you should use launch file to load world file. 

- The example world file is in `navigation/simulation-env/world_files` folder.

- Example command to run: `rosrun gazebo_ros gazebo world_files/house4.world`


# How to generate domain randomisation with random texture for models 

- Make sure you pull all models from this git and copy them into your Gazebo model folder (which is located in /.gazebo/models)

- Make sure you had backed up your orginal models in ./gazebo/models. This is important since the code will delete your original textures and replace them. You will lose your original textures if you don't back up them! 

- Open GENERATE.py and edit the path into your path of Gazebo models folder. 

- Run the GENERATE.py file: `python GENERATE.py`  This will automatically replace all old textures by new textures 

- Reload your world files. You should see your worlds are in new colors. 

- Known issues: Gazebo may immediately crash when loading a model or a world file. Fix this with: `sudo apt-get install libgazebo7-dev`
