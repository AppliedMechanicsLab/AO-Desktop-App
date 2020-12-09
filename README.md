# AO-Desktop-App

Determining the motion and acceleration field of a rigid body using measurements from four tri-axial accelerometers.

![](images/App_ScreenShot.png)

## Getting Started
It is relatively simple to run AO-Desktop-App on your own by following the instructions.

#### Download and Install Wolfram Player
In order to open the AO-Desktop-App in the main file `AO-App.cdf`, you need to install [Wolfram Player](https://www.wolfram.com/player/) on your computer. [Wolfram Player](https://www.wolfram.com/player/) is a free software developed by [Wolfram Reserch](https://en.wikipedia.org/wiki/Wolfram_Research). The player is available for Microsoft Windows, Macintosh, Linux and iOS, which can be downloaded from the following website:

https://www.wolfram.com/player/

Taking **MacOS** for example, after you open the downloaded `WolframPlayer_12.1.1_MAC_DLM` file, you should see

![](images/DownloadManager.png)

After it is finished, you need to launch the installation package and it will show

![](images/Installation.png)

When this is done, you can drag the Wolfram Player icon to the Applications folder to complete installation.

#### Download AO-Desktop-App

On the top-right corner of this page, you will see a green button called "Code". Clicking on that, you will find the option to Download ZIP of the whole project.

![](images/DownloadApp.png)

You need to unzip the file. Inside the resulted folder, you will find the main file `AO-App.cdf`, open it with [Wolfram Player](https://www.wolfram.com/player/). Upon opening the file, you see a pop-up window as shown in the following screenshot. Click on "Yes".

![](images/Initialization.png)

#### Usage example

After you have done all the above steps, you now have a user-interface to work on.

![](images/GUI.png)

You will need to input data including Postions and Directions of 

## Acceleration Data File format

* Each file contains the acceleration measurement of one accelerometer
* Format: n*4 matrix
* Units: Meter, Second, Kg

| Time | Acc_x | Acc_y | Acc_z |
|------|-------|-------|-------|
| ...  | ...   | ...   | ...   |
| ...  | ...   | ...   | ...   |


## Position and direction of accelerometers
* X1={0,0,0.83}, N={{1, 0, 0}, {0, 1, 0}, {0, 0, 1}}
* X2={0,0.1,0.75}, N={{1, 0, 0}, {0, 1, 0}, {0, 0, 1}}
* X3={0.15,0,0.75}, N={{1, 0, 0}, {0, 1, 0}, {0, 0, 1}}
* X4={-0.15,0,0.75}, N={{0, 1, 0}, {-1, 0, 0}, {0, 0, 1}}

X5={0,0,0.67}


## Initial condition
* R = I
* The position of the center of mass Xcm of the ellipsoid is (0,0,0.75)
* The initial velocity of Xcm is (0.75,0,0)
* The angular velocity of the body is (5,5,5)
