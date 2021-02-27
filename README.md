# AO-Desktop-App

Determining the motion and acceleration field of a rigid body using measurements from four tri-axial accelerometers.


<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#screenshot">Screenshot</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#download-and-install-wolfram-player">Download and Install Wolfram Player</a></li>
        <li><a href="#download-ao-desktop-app">Download AO-Desktop-App</a></li>
        <li><a href="#quick-demonstration">Quick Demonstration</a></li>
        <li><a href="#standard-workflow">Standard Workflow</a></li>
      </ul>
    </li>
    <li>
      <a href="#requirement-on-input-fields-and-data-files">Requirement on Input Fields and Data Files</a>
      <ul>
        <li><a href="#positions-and-directions-of-four-accelerometers">Positions and Directions of Four Accelerometers</a></li>
        <li><a href="#point-of-interest-poi-and-initial-conditions">Point of Interest (PoI) and Initial Conditions</a></li>
        <li><a href="#accelerometer-data-file-format">Accelerometer Data File Format</a></li>
      </ul>
    </li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#reference">Reference</a></li>
  </ol>
</details>

## Screenshot
![](images/App_ScreenShot.png)

This app is developed using Wolfram Language. It takes positions, directions and measurements of 4 accelerometers, position of point of interest and initial conditions of a rigid body as input. After performing calculation using AO-Algorithm, it outputs an interactive plot of multiple choices of variables and a simulation video showing the motion of the rigid body.

## Getting Started
It is easy to run AO-Desktop-App on your own by following the instructions:

### Download and Install Wolfram Player
In order to open the AO-Desktop-App in the main file `AO-App.cdf`, you need to install [Wolfram Player](https://www.wolfram.com/player/) on your computer. [Wolfram Player](https://www.wolfram.com/player/) is a free software developed by [Wolfram Reserch](https://en.wikipedia.org/wiki/Wolfram_Research). The player is available for Microsoft Windows, Macintosh, Linux and iOS, and can be downloaded from the following website:

https://www.wolfram.com/player

Taking **MacOS** for example, after you open the downloaded `WolframPlayer_12.1.1_MAC_DLM` file, you should be able to see

![](images/DownloadManager.png)

After it is finished, you need to launch the installation package and it will show

![](images/Installation.png)

When this is done, you can drag the Wolfram Player icon to the Applications folder to complete installation.

### Download AO-Desktop-App

On the top-right corner of this page, you will see a green button **⤓ Code**. Clicking on it, you will find the option to **Download ZIP** of the whole project.

![](images/DownloadApp.png)

You need to unzip the file. Inside the resulted folder, you will find the main file `AO-App.cdf`, open it with [Wolfram Player](https://www.wolfram.com/player/). Upon opening the file, you may see a pop-up window as shown in the following screenshot. Click on **Yes**.

![](images/Initialization.png)

After you have done all the above steps correctly, A user-interface will show up in the opened file as the following screenshot.

![](images/GUI.png)

### Quick Demonstration

For a quick demonstration, you can simply click **AO-Algorithm Calculation (using example data)** button to load example data and run the calculation. It takes around 20 seconds, depending on your CPU and memory performance, to finish the calculation. When it is finished, you will see a dialog window shown as

![](images/CalculationDone.png)

After clicking **OK**, the result will show up in the output panel. You can choose different output plots and control the video interactively.

### Standard Workflow

In this user-interface, initial input data including positions and directions of four accelerometers in global coordinate system, position where the measurement located in data file, position of Point of Interest (PoI) and initial conditions are already given based on the example data. You can change each of the input fields according to your experiments, attach data file, load and check data file and run AO-Algorithm calculation.

The standard workflow for using the AO-Desktop App contains 4 steps:
1. **Change each of the input fields** according to your experimental measurement.
2. Click on button **Attach Data File** and choose the data file on your computer to upload.
3. Click on button **Load and Check Data File**. You will be able to select and look at the plots of measurements for each accelerometer.
4. Click on button **AO-Algorithm Calculation**. When the calculation is finished, a dialog window will remind you and multiple interactive output plots and a simulation video will present in the output panel.

## Requirement on Input Fields and Data Files

### Positions and Directions of Four Accelerometers
Type positions and directions components as real numbers in the input boxes. Be aware that positions and directions vectors components are defined by projecting the vectors in global coordinate system. All length variables are in unit of meter.

If there are more than 4 accelerometers deployed in the experiments, you can select 4 of them as input by changing **Position in data file**. For example, if there are 6 measurements in your data file, and you want to select the last 4 measurements as input, you can input **3**,**4**,**5**,**6** in **Position in data file** field for **Accelerometer 1**, **Accelerometer 2**, **Accelerometer 3**, **Accelerometer 4**, respectively.

### Point of Interest (PoI) and Initial Conditions
* You need to choose a **Point of Interest (PoI)** and input its position so that the app will predict the **Acceleration**, **Velocity** and **Position** of PoI as functions of time.
* A **reference point** is required in order to define initial position and initial velocity. The reference point can be any point whose **position** and **velocity** are known in the initial time instance. It is not necessary to be the center of mass, or one of the accelerometer positions.
* The **initial angular velocity** of the rigid body should be given.
* All length variables are in unit of meter. Velocity variables are in unit of meter per second. Angular velocity variables are in unit of radian per second.

### Accelerometer Data File Format
The AO-Desktop App supports multiple data formats as inputs. You can gain insight on the supported data format by checking out the given example data files, which are located in `ExampleData` folder of this project. The example data format in files `Sample HIGH LOW G file.csv`, `Sample Blast Test csv fiel 20201109_121453-test-2.csv`, `4 PCB sensors sample file.csv` that our collaborator collected using their sensor system are all supported by this App.

## License
Distributed under the GNU General Public License. See `LICENSE` for more information.
## Contact
Wenqiang Fang - wenqiang_fang@brown.edu

Project Link: https://github.com/AppliedMechanicsLab/AO-Desktop-App
## Reference
Rahaman, Mohammad Masiur, Wenqiang Fang, Alice Lux Fawzi, Yang Wan, and Haneesh Kesari. ["An accelerometer-only algorithm for determining the acceleration field of a rigid body, with application in studying the mechanics of mild Traumatic Brain Injury."](https://www.sciencedirect.com/science/article/abs/pii/S0022509620302490) *Journal of the Mechanics and Physics of Solids* (2020): 104014.
