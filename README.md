This project includes a Dockerfile to create a Docker container image for a Python application. Below is an overview of the steps involved in building the Docker image.

- The Dockerfile starts with an official base image of python:3.9-slim, which provides a lightweight environment with Python 3.9 installed.

- A working directory /app is created inside the container, and it is set as the current working directory for the following operations.

- The entire content of the project is copied into the /app directory in the container.

- The pip package manager is used to install the required dependencies listed in the requirements.txt file. The --no-cache-dir flag is used to ensure that unnecessary package cache files are not included in the image, keeping it lightweight.

- The Docker container exposes port 8000, which is the default port where the Python application will run.

- The container runs the application by executing the Python file app.py using the python command.


To build and run the Docker container, follow these steps:

- docker build -t your-image-name .

- docker run -p 8000:8000 your-image-name

This will map port 8000 on the container to port 8000 on the host machine, allowing you to access the application in the browser at http://localhost:8000.