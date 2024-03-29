## A Demonstration of our robot DIR


#### 0. Preview of our basic navigation system!

First of all, clone it to your ros workspace source file then go to your root workspace and type catkin_make and after that source it.
Now you can follow the steps to view the navigation course!

#### 1. Launch our world and our robot

In order to start the simulation go to your terminal and hit ``` roslaunch demo_navi mybot_world.launch```. Now we want our robot to move as we want, for that hit ```rosrun teleop_twist_keyboard teleop_twist_keyboard.py```.

#### 2. Merge our two LaserScans

Because we have two LiDAR we must somehow merge their scan's so launch
```roslaunch ira_laser_tools laserscan_multi_merger.launch```.

#### 3. Launch the SLAM algorithm

Now that we started the simulation we want it to map the area, to do that we will use gmapping as our SLAM algorithm so hit ```roslaunch gmapping slam_gmapping_dn.launch``` after that go your terminal that you runned the **teleop_twist_keyboard** and navigate the area to map it seeing it from rviz.

#### 4. Save the map

After you finish mapping the area, now we must save it, for that open a new terminal and hit ```rosrun map_server map_server -f /"ENTER YOUR UNIQUE PATH"/navigation/amcl/maps/test_map```. If you have problems doing that **don't panic**, I have already saved a map just in case.If so you can skip this step and close all terminals.

#### 5. Launch amcl and move base

Finally we can see our robot moving autonomously. To begin, do again the step one without running **teleop_twist_keyboard** and step two after that we can launch amcl ```roslaunch amcl amcl_omni.launch```.


:warning: :warning: *Every bug you encouter, address it to the Issues section above.* :warning: :warning:

Thank you! :heart:


### Sources from GitHub:

- https://github.com/GuiRitter/OpenBase
- https://github.com/iralabdisco/ira_laser_tools
- https://github.com/ros-perception/slam_gmapping
- https://github.com/ros-planning/navigation- 

