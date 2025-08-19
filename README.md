# LEGATO Gripper HW Control


## Abstract
This branch provides the codebase for the basic functionality of the LEGATO Gripper, developed as part of <i>[LEGATO: Cross-Embodiment Imitation Using a Grasping Tool](https://ut-hcrl.github.io/LEGATO)</i>, along with an example script. If you find our work useful in your research, please consider [citing](#citing).


## Installation
Prior to installing dependencies, your machine must have the [Intel Realsense driver](https://github.com/IntelRealSense/librealsense) installed. From 2.54.X, the codes for T265 are removed, so we need to use the version release v2.53.1 or lower. You can use the below commands for installing the Realsense driver.
```bash
# Dependencies for the Realsense driver
apt-get install libusb-1.0-0-dev xorg-dev libglu1-mesa-dev libglfw3 libglfw3-dev
# Cloning the source code of the Realsense driver
git clone https://github.com/IntelRealSense/librealsense.git DIR_TO_LIBREALSENSE
cd DIR_TO_LIBREALSENSE
# Specifying the driver version
git checkout v2.53.1
# Setting up authorizing USB devices (You may need "sudo" commands.) 
cp config/99-realsense-libusb.rules /etc/udev/rules.d/
# Building the driver
mkdir build && cd build
cmake -D BUILD_EXAMPLES=true -D BUILD_GRAPHICAL_EXAMPLES=false -D BUILD_PYTHON_BINDINGS=true -D PYTHON_EXECUTABLE=FILEPATH_TO_PYTHON ../
make -j NUMBER_OF_PROCESSES
# Installation (You may need "sudo" commands.)
make install
```

Then, install the environments and dependencies by running the following commands.
```
pip3 install -r requirements.txt
```

Prior to running your devices, make sure your machine allow a local user to access the devices.
For devices of serail-communication, you can use the below command.
```
sudo chmod 777 /dev/ttyYOUR_DEVICE_NAME
```
For the realsense camera, you can use the below command at the Realsense driver source code.
```
sudo cp config/99-realsense-libusb.rules /etc/udev/rules.d/
```

## Usage
Before using the Gripper, an initial setup for the Dynamixel XM430 actuators is required. For convenience, it is recommended to use the [DYNAMIXEL Wizard 2.0 software](https://emanual.robotis.com/docs/en/software/dynamixel/dynamixel_wizard2/).

The actuator configuration must align with a configuration file used in the script. 
This codebase provides default configuration at [`configs/gripper.yaml`](configs/gripper.yaml).
Ensure the following settings match the values in your configuration file to avoid issues during operation.
- `BAUDRATE`: Configure the value stored at address 8 in the actuator's memory. The default value used in the codebase is  `1000000`.
- `id`: Configure the value stored at address 7 in the actuator's memory. In the default configuration of the codebase, id `1` is used for the right actuator, and id `2` is used for the left actuator.


## Usage
This branch provides example scripts for controlling the LEGATO Gripper using a RealSense T265 camera. To run the example script, use the following command:
```
python3 scripts/example.py --param_file=PATH_TO_CONFIG_FILE --streaming=STREAM_STEREO_IMAGES
```
Here, `param_file` specifies the path to the configuration file and `streaming` wnables stereo image streaming from the T265 camera when set to `True`. If no input arguments are provided, `param_file` defaults to [`configs/gripper.yaml`](configs/gripper.yaml) and `streaming` is set to `True`.

Scripts for data collection, including real-world and simulation demonstrations, can be found in LEGATO's [main repository](https://github.com/UT-HCRL/LEGATO).


## License
LEGATO is released under the [MIT License](LICENSE). For questions, please contact [Mingyo Seo](https://mingyoseo.com).


## Citing
```
@misc{seo2024legato,
    title={{LEGATO}: Cross-Embodiment Imitation Using a Grasping Tool},
    author={Seo, Mingyo and Park, H. Andy and Yuan, Shenli and Zhu, Yuke and
          and Sentis, Luis},
    year={2024},
    eprint={2411.03682},
    archivePrefix={arXiv},
    primaryClass={cs.RO}
}
```
