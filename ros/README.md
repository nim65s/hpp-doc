# HPP on ROS

## Local build

ref. [Source installation with ROS](https://humanoid-path-planner.github.io/hpp-doc/installation/ros-devel-sources.html)

## Docker

clone this repo and move into this folder, then:

```
export ROS_DISTRO=jazzy
docker build --build-arg ROS_DISTRO=$ROS_DISTRO -t hpp-ros:$ROS_DISTRO .
docker run --rm -it hpp-ros:$ROS_DISTRO
```

## Included packages

```
$ colcon graph
hpp_affordance           +
hpp_baxter                +
hpp_centroidal_dynamics    +       *
hpp_environments            +       * .*.......
hpp_plot                     +
hpp_romeo                     +
hpp_rviz                       +
hpp_tools                       +
hpp_universal_robot              +
hpp_util                          + **.*..*....
hpp_bezier_com_traj                +
hpp_pinocchio                       + **..*....
hpp_statistics                       +**.......
hpp_constraints                       +*..*....
hpp_core                               +*.*....
hpp_manipulation                        +**...*
hpp_manipulation_urdf                    +*....
hpp_python                                +***.
hpp_exec                                   +
hpp_gepetto_viewer                          + *
hpp_toppra                                   +
hpp_tutorial                                  +
```
