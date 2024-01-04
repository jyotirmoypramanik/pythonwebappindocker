This is a project for creating Python based Docker Container with Web App

This setup assumes:

Your application is called app.py and is in the same directory as your Dockerfile.

You have a requirements.txt file listing Flask

The Flask app object is named app (as is standard in Flask documentation).

Build your Docker image with 

>>docker build -t pythonwebappindocker . 

And run it with 

>>docker run -p 5001:5001 pythonwebappindocker. 

Your app will be accessible at http://localhost:5001/.








Logs >>
.....................................................................................................................................
C:\Work\docker\pythonwebappindocker>docker build -t pythonwebappindocker .
[+] Building 8.9s (10/10) FINISHED                                                                                docker:default
 => [internal] load .dockerignore                                                                                           0.0s
 => => transferring context: 2B                                                                                             0.0s
 => [internal] load build definition from Dockerfile                                                                        0.1s
 => => transferring dockerfile: 179B                                                                                        0.0s
 => [internal] load metadata for docker.io/library/python:3.9-alpine                                                        3.2s
 => [auth] library/python:pull token for registry-1.docker.io                                                               0.0s
 => [internal] load build context                                                                                           0.0s
 => => transferring context: 29.73kB                                                                                        0.0s
 => CACHED [1/4] FROM docker.io/library/python:3.9-alpine@sha256:5a8aef2661d7c9e8a4c4fc6e79c6da926f3154aac43425264b0548778  0.0s
 => [2/4] COPY . /app                                                                                                       0.0s
 => [3/4] WORKDIR /app                                                                                                      0.0s
 => [4/4] RUN pip install -r requirements.txt                                                                               5.3s
 => exporting to image                                                                                                      0.2s
 => => exporting layers                                                                                                     0.2s
 => => writing image sha256:60c1b5c7eff6de4d2f66c5c1b87cccbf395bd58aa3a4e4b20538a5971d85cbdd                                0.0s
 => => naming to docker.io/library/pythonwebappindocker                                                                     0.0s

What's Next?
  View a summary of image vulnerabilities and recommendations → docker scout quickview
.....................................................................................................................................  

..................................................................................................................................... 
C:\Work\docker\pythonwebappindocker>docker run -p 5001:5001 pythonwebappindocker
 * Serving Flask app 'app'
 * Debug mode: on
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:5001
 * Running on http://172.17.0.2:5001
Press CTRL+C to quit
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 136-636-681
172.17.0.1 - - [04/Jan/2024 17:23:16] "GET / HTTP/1.1" 200 -
172.17.0.1 - - [04/Jan/2024 17:23:16] "GET /favicon.ico HTTP/1.1" 404 -
..................................................................................................................................... 