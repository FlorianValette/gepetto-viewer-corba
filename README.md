CORBA server/client for the Graphical Interface of Pinocchio and HPP
====================================================================

Setup
-----

To compile this package, it is recommended to create a separate build
directory:

    mkdir _build
    cd _build
    cmake [OPTIONS] ..
    make install

Please note that CMake produces a `CMakeCache.txt` file which should
be deleted to reconfigure a package from scratch.


### Dependencies

The present software depends on several packages which
have to be available on your machine.

 - Libraries:
   - omniORB4 (version >= 4.1.4)
   - openscenegraph (version >= 3.2)
   - eigen3 (version >= 3.0.5) (only for C++ client)
   - urdfdom (version >= 0.3.0)
   - SceneViewer (Graphical Interface of Pinocchio and HPP)
 - System tools:
   - CMake (>=2.6)
   - pkg-config
   - usual compilation tools (GCC/G++, make, etc.)
 
### Install standalone urdfdom

In order to read urdf files (see http://wiki.ros.org/urdf for the description), one haves to install the urdfdom package which can come either along ROS library or be installed as a standalone library. Next section describes the second procedure.

urdfdom depends on both console_bridge and urdfdom_headers. The installation of both dependencies can be done with the following command lines in a terminal :
  - git clone git://github.com/ros/console_bridge.git && cd console_bridge && mkdir build && cd build && cmake .. && make && sudo make install
  - git clone git://github.com/ros/urdfdom_headers && cd urdfdom_headers && mkdir build && cd build && cmake .. && make && sudo make install
    
Finally, you just need to apply the following command line to install urdfdom library :
  - git clone git://github.com/ros/urdfdom && cd urdfdom && mkdir build && cd build && cmake .. && make && sudo make install


