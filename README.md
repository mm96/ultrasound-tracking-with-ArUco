# ultrasound-tracking-with-ArUco

STAR Ultrasound Tracking & Image acquisition, ISAT Labs, Purdue University
Mandira Marambe-- August 2018
------------------------------------------------------------------------------------------------------------------------------------
Setup (If a different computer is being used)
------------------------------------------------------------------------------------------------------------------------------------
Build OpenCV 3.4.0 on Windows with the CMake GUI and Visual Studio 2017 following instructions at :
https://github.com/kyamagu/mexopencv/wiki/Installation-%28Windows%2C-MATLAB%2C-OpenCV-3%29
mexopencv compilation directions can also be found at the same link.
Run all programs as administrator when compiling.
Make sure the dev folder instructions below are also followed
------------------------------------------------------------------------------------------------------------------------------------
Matlab function
------------------------------------------------------------------------------------------------------------------------------------
The Matlab function Ultrasound.m returns the transducer position coordinates with respect to the camera and the ultrasound image in 
RGB format
Notes:
-In this folder the file can be found at mexopencv>opencv_contrib>samples
-Uses the ArUco marker library with mexopencv 
-Camera calibration for Logitech USB camera done using 5x7 board generated from the 4x4_1000 dictionary (board4.jpg in the folder), 
with provided demo code aruco_calibrate_camera_demo.mat in mexopencv>opencv_contrib>samples
-For ultrasound image acquisition via EchoWave II,RUN BOTH MATLAB AND ECHOWAVE II AS ADMINISTRATOR
-**Matlab Computer Vision Toolbox Required (included in R2018a version)
-Use the same marker ids and positions/orientations so that it would not be necessary to make changes in computing the cooordinates
------------------------------------------------------------------------------------------------------------------------------------
dev
------------------------------------------------------------------------------------------------------------------------------------
The folder dev contains mexopencv libraries for matlab mex. The path reference to the folder in the program (C:\dev) must be changed 
if the folder location changes.
 *mexopenCV dll files must be in the same location as wrappers (already moved to mexopencv>opencv_contrib>+cv in the included folder)
Also included in dev are the c# codes (imageSaving.cs USocketServer.cs) that have been used with the HoloLens in STAR and may be 
useful in setting up communication.
------------------------------------------------------------------------------------------------------------------------------------
ArUco
------------------------------------------------------------------------------------------------------------------------------------
ArUco markers can be generated at http://chev.me/arucogen/
A pdf of the ArUco library documentation is included in this folder.
------------------------------------------------------------------------------------------------------------------------------------
EchoWave Ultrasound Acquisition
------------------------------------------------------------------------------------------------------------------------------------
EchoWave (http://www.telemedultrasound.com/echo-wave-ii/?lang=en) must be run as administrator. Use the 'Cine' (F11) option on the 
echowave software to enable obtaining the images if it does not work otherwise.
The program uses AutoInt1Client.dll (C:\Program Files (x86)\TELEMED\Echo Wave II\Config\Plugins) in the echowave plugins to communicate with EchoWave. Make sure that the paths are correctly
specified in the matlab program. 
While real time image acquisition has been included in the main program, ultrasound_acquisition.mat in mexopencv>opencv_contrib>samples 
contains the stand alone code obtaining the images (however this is not in real time).
------------------------------------------------------------------------------------------------------------------------------------\

If you catch anything I missed, drop  me a text/email at mmarambe@smith.edu :D:D
