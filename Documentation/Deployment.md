# Deployment Guide

## System Requirements
- Epic Games Launcher
  - Needed to install unreal engine
- Visual Studio Community
  - THIS IS DIFFERENT FROM VS CODE. For compatability purposes, you need some version of Visual Studio, not VS Code. VS community is the free version.

## Deployment Steps

### 1. Clone GitLab repository
- In Git Bash, run the command <code>git clone https://github.com/dapark3/SpoofDetectorApp.git</code>

### 2. Rebuild solution file
- Unreal engine projects use Visual Studio solution files to point to engine components
  - If you pull a repository from the web, the solution file will most likely not be accurate for your local machine
- Open the 'ueui' folder
  - Right click on the file with the '.uproject' extention
  - Click 'Show more options' if on Windows 11
  - Click 'Generate Visual Studio project files'

## 3. Run the Project
- The project can be opened directly from the folder by clicking the '.uproject' file
- As well, you can launch the project from the Epic Games Launcher
  - Open Epic Games, log in, click Unreal Engine
  - Once in the UE menu, open the project and wait for it to load

- Now you should be viewing a topographic map in unreal!

### 4. Troubleshooting  (Need 2 change)
 - Check console to ensure web page is recieving data from the server
 - Check to make sure 'cesiumInput.json' exists
 - Check to ensure paths are correct and code is not breaking in console
       
### 5. Critical or Vulnerable Components: (Need 2 change)
 - Cesium relies on 'cesiumInput.json' to write data points to the map
 - handle_server_data requests the data from a server
 - DataProccesor takes in the data and gives each drone instance a rating, then outputs the data
