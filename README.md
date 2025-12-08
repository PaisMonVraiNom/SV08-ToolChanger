# SV08-ToolChanger
Custom 6 toolhead tool changer based on the Sovol SV08

***
Disclaimer: I am not an electrician, engineer, software developer or the like. This repository is not a professional recommendation.
I am not affiliated with any of the products or individuals mentioned in this project
***

Here will contain my 3D printer files, STLs and the slicer gcode sections I used to create this printer. STLs created by others will he uploaded and credited along with comments on edits from the originals. Should the creators of the files request, I will remove files not created by me.

Steps which must be completed on your SV08 to use these config files:
1. Convert SV08 to mainline Klipper - https://github.com/Rappetor/Sovol-SV08-Mainline
2. Install ToolChanger module for Klipper - https://github.com/viesturz/klipper-toolchanger

The layout of my Printer_Data folder is unorthodox but it all functions as is. 

As of version 1.0 there are a few QOL changes that are required in the macros:

1. Pause_print needs updating. I currently use Pause_base (the renamed original pause macro)
2. Initial purge line is always printed using the currently equipped tool - even if that tool is not in the print or not to be used first - this print head is then left at the 130 degree idle temp for the duration of the print.
