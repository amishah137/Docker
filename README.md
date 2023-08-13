# Docker
### Why container?
- A way to package an application with its dependancies and configuration.
- Portable artifact, easily share and move this package to any environment.
- Makes developmnet and deployment more easy and efficient.

### Docker vs Virtual Machine

### Basic Structure of dockerfile
```
FROM python
COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt
CMD pyhton app.py
```

To build the image
```
docker build -t myImage:1.0.0 .
```

To run the docker image
```
docker run myContainerName -p 5000:5000 myImage:1.0.0
```
