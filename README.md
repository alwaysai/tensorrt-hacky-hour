# TensorRT Applications

![NV_TensorRT_Visual_2C_RGB-625x625-1](https://user-images.githubusercontent.com/21957723/96040050-82ba7e80-0e1e-11eb-8e94-a29f281acd0c.png)


This alwaysAI applications set uses TensorRT binaries to do the local infernecing on a NVIDIA Jetson device, these binaries can be found in the alwaysAI model catalog.  The model will start with TRT and end with the Jetson device name it should be run on, for example nano.  These binaries are the most efficient way to do infernecing on NVIDIA Jetson device.  Currently alwaysAI support TensorRT binaries for Jetson Nano, TX2 and Xavier XM.  

![TRT-FLOW](https://user-images.githubusercontent.com/21957723/96040262-d88f2680-0e1e-11eb-871b-c28884bae089.png)



## Repo Programs
| Folder                     	| Description                                                                                              	|
|----------------------------	|----------------------------------------------------------------------------------------------------------	|
| license-vehicle-detection   | Program detects vehicles and license plates, currently setup to work with Jetson Nano|
| distance-between-hands 	    | Program detects distance between hands in meters, this application needs a Intel Realsense camera to run and is setup to work with Jetson Nano|


## Setup

This app requires an alwaysAI account. Head to the [Sign up page](https://www.alwaysai.co/dashboard) if you don't have an account yet. Follow the instructions to install the alwaysAI tools on your development machine.

Next, create an empty project to be used with this app. When you clone this repo, you can run `aai app configure` within the repo directory and your new project will appear in the list.

## Usage

Once the alwaysAI tools are installed on your development machine (or edge device if developing directly on it) you can run the following CLI commands:

To set up the target device & install path

```
aai app configure
```

To install the app to your target (make sure you use the aai app models add command to add the current TensorRT model)

```
aai app install
```

To start the app

```
aai app start
```
