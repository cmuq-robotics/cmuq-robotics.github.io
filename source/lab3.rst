Lab 3: ARTag tracking with Alvar
=============================================================================

An AR-tag is a fiducial marker system that can help with robot navigation and perception challenges, serving as a point of reference for moving in the environment and detecting obstacles.

In this lab, we will use `ar_track_alvar` package for detecting individual markers.

Getting Started
----------------------
Install the `ar_track_alvar` ros package in your VM.

.. code-block:: bash

   sudo apt install ros-melodic-ar-track-alvar

Clone the example code into your catkin workspace:

.. code-block:: bash

   cd ~/catkin_ws/src
   git clone https://github.com/EduardoFF/ar-track-alvar-example.git


Launching the example
--------------------------------------------------

Connect to one of the robots and edit the file `connect_robot.sh` with the correct values.

Open a new terminal window and set the environment variables:

.. code-block:: bash

   source ~/connect_robot.sh


Use the tool `rostopic` to see the list of topics currently used in the network:

.. code-block:: bash

   rostopic list

Launch the example code:

.. code-block:: bash

   roslaunch ar-track-alvar-example ar_track_alvar.launch


Visualizing the markers in RViz
-----------------------------------------

You can use **RViz** to visualize the markers.

First we need to run `turtlebot3_remote.launch` to load the 3D model and the description of the robot (otherwise, it won't show in RViz and the TF won't work properly).

In a new terminal, set the environment variables and run:

.. code-block:: bash

   source ~/connect_robot.sh
   roslaunch turtlebot3_bringup turtlebot3_remote.launch


To launch rviz with a predefined configuration for the turtlebot3, open another terminal and run:

.. code-block:: bash

   source ~/connect_robot.sh
   rosrun rviz rviz -d `rospack find turtlebot3_description`/rviz/model.rviz


You should now have an RViz window open showing the TurtleBot3 (the real one!).


Change the `Fixed Frame` to `base_link` in the `Global Options`.

Add the markers using the topic `/objects/visualization_markers`

Now you can see the markers!
