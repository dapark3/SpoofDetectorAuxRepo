(You can also deploy your environment using docker via 'Alternate Deployment via Docker')

# Deployment Guide

## System Requirements
- PyCharm Community Edition or any IDE installed on the development machine.
- Git 
- Pip & Npm (Package managers to install dependencies)

## Deployment Steps

### 1. Clone the Repository  
 - In Git Bash, run the command <code>git clone https://github.com/dapark3/SpoofDetectorApp.git</code>

### 2. Open Project in PyCharm  
- Open PyCharm. Select "Open" from the main menu.  
- Navigate to the cloned repository directory and select it.

### 3. Configure PyCharm Project  
 - Ensure that your PyCharm project is configured with the correct SDK. This project uses Python 3.11.  
   - Set up a new Python SDK if not configured.
   
### 4. Install dependencies
 - Open a CLI instance
 - Python:
   - In the Model directory, run <code>pip install -r requirements.txt</code>
 - Node:
   - In the View directory, run <code>npm install</code>

### 4. Run the Application   
 - Locate node.js in View
 - PyCharm allows devs to run a localhost with a single-click in a web browser
 - Alternatively, you can CD into View using a CLI and run <code>node node.js</code>
   - The webpage can be viewed from localhost:3000
 - The application should run and display a topographic map with individual drone data points

### 5. Troubleshooting  
 - Check console to ensure web page is recieving data from the server
 - Check to make sure 'clean_data.json' exists
 - Check to ensure paths are correct and code is not breaking in console
       
### 6. Critical or Vulnerable Components:
 - Cesium relies on 'clean_data.json' to write data points to the map
 - handle_server_data requests the data from a server
 - DataProccesor takes in the data and gives each drone instance a rating, then outputs the data


# Alternate Deployment via Docker

## System Requirements
- An IDE. VS and Pycharm both have Docker extentsions which are useful for building images and running containers
- <a href="https://docs.docker.com/desktop/">Docker Desktop</a>

## Deployment Steps

### 1. Clone the Repository  
 - In Git Bash, run the command <code>git clone https://github.com/dapark3/SpoofDetector.git</code>

 ### 2. Open Project in an IDE or a CLI
- You can build a docker image either using an IDE with extensions or directly through the command-line
- For these instructions, we will default to using PyCharm as the IDE
- Open the cloned repository folder (Open the project in your IDE or CD into it through the command-line)

 ### 3. Run Dockerfile
- IDE (PyCharm):
  - Click the Dockerfile, then click "Edit 'Dockerfile'"
  - Set the image tag to whatever name you choose
  - Click 'Modify Options', then click 'Bind Ports -p'
  - Set 'Bind Ports' to 3000:3000
  - Click apply
  - Click "Build Image for 'Dockerfile'"
    - This will create an image with the set tag and binded port 3000
    - This process may take around a minute
  - Run the Dockerfile
    - This will create a container of the image that can then be worked on
- CLI:
  - From the root directory, run <code>docker build -t 'tag' -p 3000:3000 ./</code>
    - This will build an image with the tag 'tag' and binded to port 3000
  - Next, run <code>docker run 'tag'</code>
    - This will create a container of the image 'tag'
      
- Now, you should have a container of the built docker image.
  - The webpage can be viewed from localhost:3000

### 4. Troubleshooting  
 - Check console to ensure web page is recieving data from the server
 - Check to make sure 'cesiumInput.json' exists
 - Check to ensure paths are correct and code is not breaking in console
       
### 5. Critical or Vulnerable Components:
 - Cesium relies on 'cesiumInput.json' to write data points to the map
 - handle_server_data requests the data from a server
 - DataProccesor takes in the data and gives each drone instance a rating, then outputs the data
