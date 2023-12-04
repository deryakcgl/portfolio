# STM32F407VG Discovery Keil Settings
To program STM32 with Keil, we open the Keil / Pack Installer tool 
and search for STM32F407VG in Devices. We download the packages from 
the Pack option. For simple projects, it is sufficient to install 
AMP, CMSIS, ARM Compiler and MDK Middleware packages. 
Apart from this, we download STM32's own drivers. 
Most STM32 example programs we will find on the 
Internet were created with version 1.08 of the Keil STM32 library.
For this reason, I used version 1.08 when programming STM32,
except for the projects I created with CUBEMX. 
Version 1.08 can be downloaded by clicking Previous. 
After the necessary drivers are downloaded, follow the 
Project/New uVision Project path via Keil to create a new project. 
STM32F407VG device is selected in the window that opens.
A window named Manage Run Time Environment opens.
This is where we will select the necessary libraries for the program
we will write. After selecting the required libraries, the project is opened by pressing OK.
In the Project window on the left, right-click on the Source Group and select 
Add New Item to Group. From here, “main.c” is created.
This is the C file in which we will write the program codes.
After this stage, it is necessary to make the necessary settings for STM32. 
This stage is very important because if it is not done, the program will give
an error when being transferred to STM32.
Options for target is selected.
It is changed from Target to Xtal 8.
If the STM32 Utility program will be used,
Create Hex File is selected from OUTPUT to create a hex file.
Necessary definitions for STM32 are made in the C/C++ tab where it says Define.
[ USE_STDPERIPH_DRIVER, STM32F4XX, HSE_VALUE=8000000 ]
In the same tab, the location of the file is selected in the include paths section.
In the Debug tab, Use: ST Link Debugger should be selected.
If Use Debug Driver is selected in the Utility tab, it is removed and ST Link Debugger is selected.
When you click on Settings here and go to the Debug tab, you should see your own device.
To load the program to STM32, it is first compiled with the F7 key and then loaded with F8.
Installing the program using STM32 Utility;
Connect to the device with Connect to target. The hex file is opened with Open File. 
With Program Verify, the program is transferred to STM32.
