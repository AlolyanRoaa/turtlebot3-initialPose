# turtlebot3 initial Pose


applying a python script to specify an initial position for turtlebot3 burger robot.This document is completely dependent on the previous document (Creating-a-map-using-Turtlebot3-and-SLAM), it is recommended to reviewing it before starting.

so, [click here](https://github.com/AlolyanRoaa/Creating-a-map-using-Turtlebot3-and-SLAM) to go to its repository.


## Outline


- Preparations
- New position
- Demo

## Preparations

we have to clone the [github repository](https://github.com/markwsilliman/turtlebot) which contains *go_to_specific_point_on_map.py* script that we are going to use.


in the workstation run these commands 


```bash
mkdir ~/forinitial
cd ~/forinitial/
git clone https://github.com/markwsilliman/turtlebot/
```

![]()

now run the simulation with the map created previously


```bash
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
```

and in new terminal


```bash
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
```


## New position

after estimating the initial pose, to get the dimension of the new position go to RViz window in panels tap check on selection box.


then the selection panle will appears on the left side of the window, now you can select a specific location on the map by using ![]() tool

![]()


on the selection panel you will get x, y coordinates for your position. on *go_to_specific_point_on_map.py* script you must change the position to these values.


to open the script, refer to the directory that made earlier by using `cd` command. then run


```bash
gedit go_to_specific_point_on_map.py
```


![]()


then change the values of x and y, and save changes.

![]()


## Demo

run the script by using this command


```bash
python go_to_specific_point_on_map.py
```

![]()


the robot will move to the specified location


![]()


![]()












