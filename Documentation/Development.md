# Development Environment Manual

## Backend & Frontend
- Frontend
  - Node.js to run web server for web page
  - Serve-index middleware for directory listings
- Backend
  - Python
    - json, os, logging, csv, datetime, and requests libraries
    - Unittest for testing purposes


## Installing Prerequesites
- PyCharm Community Edition (Any IDE works, PyCharm works well with Python)
  - [https://www.jetbrains.com/idea/download/?section=windows](https://www.jetbrains.com/pycharm/download/?section=windows)
- Git
  - [https://git-scm.com/downloads](https://git-scm.com/downloads)
- Pip & Npm (Package managers for dependencies)
  - [https://pypi.org/project/pip/](https://pypi.org/project/pip/)
  - [https://nodejs.org/en/download/](https://nodejs.org/en/download/)


## Replicate the Development Environment

### Clone GitLab repository
- In Git Bash, run the command <code>git clone https://github.com/dapark3/SpoofDetectorApp.git</code>

### Installing dependencies
 - Open a CLI instance
 - Python:
   - In the Project/src/Model directory, run <code>pip install -r requirements.txt</code>
 - Node:
   - In the Project/src/View directory, run <code>npm install</code>


## Linting
- This project uses two linters
  - EsLint for the Frontend
  - Ruff for the Backend
- GitHub automatically runs the linters through an action workflow
  - The workflow installs the required dependencies
  - The workflow runs both linters automatically and fixes any issues
  - The linters also act as formatters and formats the code


## Testing
- Open a CLI instance
- CD into Project/src/Model
  - Run <code>coverage run -m unittest discover</code>
  - Then, run <code>coverage report --omit='test_*'</code>
    - This creates a coverage report of the unit tests
    - "--omit='test_*'" omits the test files from the coverage report

  
## Run the Project
- Locate node.js in Project/src/View
- PyCharm allows devs to run a localhost with a single-click in a web browser
- Alternatively, you can CD into Project/src/View using a CLI and run node node.js
 - The webpage can be viewed from localhost:3000

- Now you should be viewing a topographic map! Look around for drones!


## Containerization via Docker
- Instead of manually installing the dependencies and running the project, you can simply build a docker image and run a container from the image
- This can be done through an IDE with a docker extension (VS, PyCharm) or through a CLI

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

