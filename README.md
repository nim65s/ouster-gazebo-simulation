# ouster_gazebo_simulation

package for the simulation of the Ouster OS1-64 with ros and gazebo.

Part of the code is from the work of Wil Selby ([link](https://github.com/wilselby/ouster_example)).

# Requirements

If you want to use the GPU acceleration for the Ouster lidar simulation, you need to use a version of `Gazebo` including a GPU usage fix. For the `Kinetic` version and the `Melodic` version of ROS apt repositories (`Gazebo` 7.0.0 and 9.0.0), you will need to install up-to-date packages (from the OSRF apt repository, see note 1 below) or to build `Gazebo` from source. The minimum versions of `Gazebo` are:
* for ROS `Kinetic`, `Gazebo` 7.14.0 or newer
* for ROS `Melodic`, `Gazebo` 9.4.0 or newer

If you forget to disable the GPU acceleration (see note 2 below) using an unadapted version of `Gazebo`, here are the problems you can encounter:
 * with `Gazebo7` version under 7.14.0, the simulated data can have a spherical appearance.
 * with `Gazebo9` version under 9.4.0, we observed crashes during the development of the package.

> ***NOTE 1:*** To install a up-to-date package from the OSRF apt repository, you can follow , following [this guide](http://gazebosim.org/tutorials?tut=install_ubuntu) (replacing <code>sudo apt-get install <b>gazebo11</b></code> with the wanted version of `Gazebo`).
> ***NOTE 2:*** To disable GPU acceleration you can use the `gpu` parameter of the `macro` when adding the lidar to your `Xacro` model (setting it to `false` will disable the GPU acceleration).
[![Pipeline status](https://gitlab.laas.fr/gepetto/ouster-gazebo-simulation/badges/master/pipeline.svg)](https://gitlab.laas.fr/gepetto/ouster-gazebo-simulation/commits/master)
[![Coverage report](https://gitlab.laas.fr/gepetto/ouster-gazebo-simulation/badges/master/coverage.svg?job=doc-coverage)](http://projects.laas.fr/gepetto/doc/gepetto/ouster-gazebo-simulation/master/coverage/)

