# Docker
### Why container?
- A way to package an application with its dependancies and configuration.
- Portable artifact, easily share and move this package to any environment.
- Makes developmnet and deployment more easy and efficient.

### Docker vs Virtual Machine
  ![image](https://github.com/amishah137/Docker/assets/11003645/2a36ffc9-68dd-466b-b3cf-41d2bc4d71c9)

  - Docker virtualizes the application layer and VM virtualizes complete OS.
  - Docker image size is usually small whereas VM size is huge.
  - Docker containers start and run much faster than VM as Docker only interacts with OS kernel and VM has an application and its own OS kernel and takes time to start both of them.
  - VM does not have compatibility issue. In docker, compatibility issue may exist. 

### Basic Structure of dockerfile
  ```
  FROM python
  COPY . /app
  WORKDIR /app
  RUN pip install -r requirements.txt
  CMD pyhton app.py
  ```
  - 'FROM': Specify the base image to work with.
  - 'COPY': To copy contents of src directory (. - current directory) to destination directory (/app).
  - 'WORKDIR /app': The absolute path to use as working directory (/app).
  - 'RUN': an image build step, the state of the container after a RUN command will be committed to the container image. A Dockerfile can have many RUN steps that layer on top of one another to build the image.
  - 'CMD': CMD is the command the container executes by default when you launch the built image.

To build the image
```
docker build -t myImage:1.0.0 .
```

To run the docker image
```
docker run myContainerName -p 5000:5000 myImage:1.0.0
```
