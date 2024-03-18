# Development Environment Manual

## Tech Stack
- Unreal Engine
  - Uses the Cesium plugin


## Installing Prerequesites
- Epic Games Launcher
  - Needed to install unreal engine
- Visual Studio Community
  - THIS IS DIFFERENT FROM VS CODE. For compatability purposes, you need some version of Visual Studio, not VS Code. VS community is the free version.


## Replicate the Development Environment

### Clone GitLab repository
- In Git Bash, run the command <code>git clone https://github.com/dapark3/SpoofDetectorApp.git</code>

### Rebuild solution file
- Unreal engine projects use Visual Studio solution files to point to engine components
  - If you pull a repository from the web, the solution file will most likely not be accurate for your local machine
- Open the repository folder
  - Right click on the file with the '.uproject' extention
  - Click 'Show more options' if on Windows 11
  - Click 'Generate Visual Studio project files'


## Testing
- Open a CLI instance
- CD into /Model
  - Run <code>coverage run -m unittest discover</code>
  - Then, run <code>coverage report --omit='test_*'</code>
    - This creates a coverage report of the unit tests
    - "--omit='test_*'" omits the test files from the coverage report

  
## Run the Project
- The project can be opened directly from the folder by clicking the '.uproject' file
- As well, you can launch the project from the Epic Games Launcher
  - Open Epic Games, log in, click Unreal Engine
  - Once in the UE menu, open the project and wait for it to load

- Now you should be viewing a topographic map in unreal!
