# TensorRT Applications

![NV_TensorRT_Visual_2C_RGB-625x625-1](https://user-images.githubusercontent.com/21957723/96040050-82ba7e80-0e1e-11eb-8e94-a29f281acd0c.png)

This alwaysAI applications set uses TensorRT binaries to do the local inferencing on a NVIDIA Jetson device, these binaries can be found in the alwaysAI model catalog.  The model will start with TRT and end with the Jetson device name it should be run on, for example nano.  These binaries are the most efficient way to do inferencing on NVIDIA Jetson device.  Currently alwaysAI supports TensorRT binaries for Jetson Nano, Xavier NX, and AGX Xavier.

![TRT-FLOW](https://user-images.githubusercontent.com/21957723/96040262-d88f2680-0e1e-11eb-871b-c28884bae089.png)

## Repo Programs
| Folder                     	| Description                                                                                              	|
|----------------------------	|----------------------------------------------------------------------------------------------------------	|
| license-vehicle-detection   | Program detects vehicles and license plates, currently setup to work with Jetson Nano|
| distance-between-hands 	    | Program detects distance between hands in meters, this application needs an Intel RealSense camera to run and is setup to work with Jetson Nano|

## Requirements
* [alwaysAI account](https://alwaysai.co/auth?register=true)
* [alwaysAI Development Tools](https://alwaysai.co/docs/get_started/development_computer_setup.html)

## Usage

Once the alwaysAI tools are installed on your development machine (or edge device if developing directly on it) you can run the following CLI commands:

To perform initial configuration of the app:

```
aai app configure
```

If you're running on a Jetson device other than a Nano, add the model from the catalog and update your app. For example, for an Xavier NX:

```
aai app models add alwaysai/TRT_ssd_mobilenet_v1_coco_vehicle_license_xavier
```

Then update `app.py` to reflect the new model ID.

To prepare the runtime environment and install app dependencies:

```
aai app install
```

To start the app:

```
aai app start
```

## Support
* [Documentation](https://alwaysai.co/docs/)
* [Community Discord](https://discord.gg/z3t9pea)
* Email: support@alwaysai.co
