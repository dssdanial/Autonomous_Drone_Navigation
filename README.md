# Semi Autonomus Drone Navigation

Introduction
=============

The simulation process involves creating a virtual environment using Unreal Engine 4.27 and the AirSim plugin, which provides a high-fidelity simulation of drone flight and sensor data collection. The environment includes various types of crops, terrain, and obstacles that the drone must navigate around. The simulation allows for the testing and validation of different drone sensors, including RGB and thermal cameras, LIDAR, and ultrasound sensors.

The simulation allows for testing and validation of drone-related algorithms and techniques, such as object detection, path planning, and data collection. It also enables the development of new features and applications that can be integrated into the drone's hardware and software. Additionally, the use of AI and machine learning algorithms in the simulation can improve the accuracy and efficiency of data collection and analysis.

<figure>
  <img src="https://user-images.githubusercontent.com/80394968/224868977-cf1cd102-3fbf-4de7-96cc-528c55794761.png" alt="Image 1">
</figure>
<p align="center">
  Drone farming environment
</p>

Requirments
===========

<img src="https://user-images.githubusercontent.com/80394968/224969515-c77bdfe8-f115-4f14-bb31-0ca5ce6cbf19.png" width="30" /> System 
-------

* Win OS 10 or 11 
* DirectX 11 compatible graphics card with 16 GB video RAM
* CPU with at least 4 cores
* SSD hard drive with at least 20 GB free space 

<img src="https://user-images.githubusercontent.com/80394968/224971035-f404cb16-4c9c-437e-b70d-61cad87f9847.png" width="25" /> Tools
-----
* Unreal Engine 4.27
* AirSim (new version)
* Open CV for Python
* Microsoft visual studio 22 
* Desktop Development with C++ & Developer Command Prompt for VS 2022
* NET Framework SDK (Windows 10 SDK 10.0.19041)

Installation
=============
* Install Epic game launcher & [Unreal Engine 4.27](https://docs.unrealengine.com/4.27/en-US/Basics/InstallingUnrealEngine/)
* Download [AirSim](https://microsoft.github.io/AirSim/) package 
* To download the project files, go to [Google Drive](https://drive.google.com/drive/folders/1HEl6NDDz8kOuERAFpLMrJWBNcjAKZSu_?usp=share_link) and look for a file called "Assignment VR". Inside, you'll find two zip folders and a script called "setting.json".

* The "Drone_VR" folder contains the Unreal Engine environment. Extract it into the ``Documents\Unreal Projects`` directory.

* The "Drone_shell" folder contains the main.cpp and Python scripts. Extract it into the AirSim folder you downloaded. Note that there's already a file named "Drone_shell" inside the AirSim package, so you'll need to replace it with the one from the project files. The program is written in C++, so you'll need to compile it before running it.
 
* After adding the Drone_shell file and extracting it, you can use the ``Developer Command Prompt VS22`` to navigate to the repository where you put the AirSim package. Then, you can call ``build.cmd`` to compile the program and generate the "Plugin" folder for Unreal Engine.
* Copy the "Drone_shell" file from the AirSim package and paste it into the ``Document\Unreal Project\Drone_VR`` folder.
* Copy the "Plugin" file from the "AirSim\Unreal" package and paste it into the ``Document\Unreal Project\Drone_VR`` folder. There may already be a "Plugins" folder inside the "Drone_VR" directory. Simply replace it with the new one from the AirSim package.
* Right-click on the ``Dorne_VR.uproject`` file in the Drone_VR folder and select `Generate Visual Studio project files` to perform the final compilation of the project with the newly added files.
* Open the "Drone VR.sln" file and ensure that the configuration solution is set to "Debug Game Editor" and the solution platform is set to "Win64" and start the project. The initial compilation may take some time. If the Unreal environment does not open, try restarting the project.
* If you're using the AirSim plugin for the first time in Unreal Engine, follow these steps:
  * Check if the AirSim plugin is installed by going to Edit/Plugins and searching for "AirSim".
  * Go to Window/World Settings and set the GameMode Override to AirSimGameMode.
  * When you first time play the game, Unreal will ask you which type of vehicle you want to use with AirSim. It's not really important which option you choose, just select one and start playing.
  
  _Note: To ensure optimal performance, it's recommended to uncheck the "Use Less CPU when in Background" option in Unreal Editor. To do this, go to Edit/Editor Preferences, search for "CPU", and uncheck the option. If you don't do this, Unreal Engine will be slowed down dramatically when the window loses focus._

* Stop the game and close the environment. In your `Documents` folder, you can find a folder named AirSim, which is created automatically after the first run.
Inside the folder, there is a file named `settings.json`, where you can define the properties for your vehicle, sensors, cameras, and more.
Delete the existing `settings.json` file and replace it with the file you downloaded from our Google Drive.

* After replacing the `setting.json` file, you need to reopen the `Drone_VR.sln` file in your Unreal project folder. Once the file is open, the changes in the new `setting.json` file and the existing file will merge automatically.
* Play again `Drone_VR.sln`, open the environment from the bottom window where you can find the Content folder. Inside the Content folder, you will find a map named `Drone_AirSim_Controller.umap`. Try to open it, and the environment will appear. You can now play the game and see the environment, as shown in above figure.
* To connect to the AirSim drone in the Unreal Engine environment, you need to open the DroneShell.sln file from the DroneShell folder in your project file. Make sure the solution configuration is set to "Debug" and the solution platform is set to "x64", and then start it. A shell window will appear where you can find the connection to connect to the AirSim drone. Once connected, you can enter commands and enjoy the game. 

_Note: The DroneShell algorithm uses a single communication channel, so every time you send a command, you have to wait for a response. This condition makes it difficult to get real-time feedback from the drone._

Usage
=============

* All avabile command for drone are showned in following table:

| Function | ability|
|------------------|------------------|
|CircleByPath|Make the drone go in a circle using path commands|
|GetImage|Get an image from the simulator|
|GoHome|Go back to the takeoff point and land|
|Land|Land the drone|
|MoveByManual|Move using Keyboard|
|MoveToPosition|Move to x,y,z with specified velocity|
|PlayPose|Use data registered via recordpose() to reach set of points|
|RecordPose|User can append a single pose snapshot and create mauale path|
|RequestControl|Take offboard control of drone|
|SensorFeedback|Retrieve feedback from the Barometer, GPS, and IMU  and Lidar sensors|
|SquareByPath|Make the drone go in a square using path commands|
|TakeOff|Drone takeoff to a default altitude|
|help,?|Help on the supported commands|
|quit,q|Exit the shell|
|#|Comment out the line|

                                  



Video
=============

Members
=============
| Github-page | Email |
|------------------|------------------|
| [Mohammad Reza Haji Hosseini](https://github.com/mrhosseini75) | mrhhosseini75@gamil.com |
| [Bouazza El Moutaouakli](https://github.com/ElSibo)  | siboasa@gmail.com |
| [Danial Sabzevari](https://github.com/dssdanial)  | electrical.eng.ds@gmail.com |
| [Parinaz Ramezanpour](https://github.com/ParinazRmp)  | parinaz.ramezanpoor0@gmail.com |

