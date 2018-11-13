AADC 2018 - Team AlpaKa
===============================================
This is the entry of team AlpaKa for the [Audi Autonomous Driving Cup](https://www.audi-autonomous-driving-cup.com/) 2018.

Please consider the license information provided with this repository.
You should have received a copy [LICENSE.md](LICENSE.md).

Team AlpaKa is supported by the FZI Foschungszentrum Informatik Karlsruhe. General information regarding the AADC support at the FZI, e.g. publications and code description, can be found here:

**[Audi Autonomous Driving Cup at www.fzi.de](http://url.fzi.de/aadc)**


Dependencies
-----------------------------------------------

Team Alpaka based its entry on many open source libraries:

* [ROS](https://ros.org) (component communication, visualization, ...)
* [OpenCV](https://opencv.org/) (image handling)
* [oadrive](https://github.com/fzi-forschungszentrum-informatik/oadrive) (core driving functionalities)
* [ros_oadrive](https://github.com/fzi-forschungszentrum-informatik/ros_oadrive) (ROS wrapper for oadrive)
* [adtf_ros](https://github.com/fzi-forschungszentrum-informatik/adtf_ros) (ROS bridge for ADTF)
* [darknet_ros](https://github.com/leggedrobotics/darknet_ros) (YOLO (vehicle and blue lights detection))


The projects *oadrive*, *ros_oadrive* and *adtf_ros* have been extensively further developed to fit to the competition requirements 2018.

We describe the structure of the main components below.


Structure
-----------------------------------------------

### aadc2018 (this repository)
This repository contains a description of the general project and the basic ADTF config that was used in the cup. This is the entry point of the code and depends on all the other repositories.

### oadrive
This repository holds a family of C++ libraries, containing the general program logic to drive a car, independent of any middleware (e.g. ADTF or ROS). 
It can be found here: https://github.com/fzi-forschungszentrum-informatik/oadrive
    
### ros_oadrive
This repository contains ROS wrappers for the libraries contained in oadrive. It brings everything together and allows communication between the different modules.
It can be found here: https://github.com/fzi-forschungszentrum-informatik/ros_oadrive

### adtf_ros
This connects a ROS interface to ADTF, which allows for communication with ros_oadrive. It corresponds to the aadcUser folder in the default AADC vehicle system configuration.
It can be found here: https://github.com/fzi-forschungszentrum-informatik/adtf_ros
    

Setup
-----------------------------------------------

While most of the dependencies can be installed via the package manager on a recent Ubuntu linux system, the libraries oadrive, ros_oadrive and adtf_ros have to be downloaded from github and built from source.

1. Install an Ubuntu linux system with all dependencies (Tested with Ubuntu 16.04).  See http://wiki.ros.org/kinetic/Installation/Ubuntu for an entry point on installing ROS.
2. Clone and follow the instructions in the [*oadrive*](https://github.com/fzi-forschungszentrum-informatik/oadrive) repository to set up and install oadrive.
3. Clone and follow the instructions in the [*ros_oadrive*](https://github.com/fzi-forschungszentrum-informatik/ros_oadrive) repository to set up and install ros_oadrive.
4. Clone the [*adtf_ros*](https://github.com/fzi-forschungszentrum-informatik/adtf_ros) repository inside the aadcUser folder of the AADC vehicle.
5. Load the UserConfiguration ADTF project inside this repository in ADTF.


Contact:
-----------------------------------------------
* Team AlpaKa: tks-aadc2018@listserv.fzi.de
* [Audi Autonomous Driving Cup at FZI website](http://url.fzi.de/aadc)
