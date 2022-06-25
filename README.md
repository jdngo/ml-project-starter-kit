Use this repo to easily set up JupyterLab in a Docker container that you can access via localhost in your browser. You can add additional libraries in requirements.txt that will be installed when building the Docker image.

## Build Docker Image
```
cd ml-project-starter-kit

docker build -t ml-project-starter-kit .
```

## Run Docker Container
The -v flag is used to mount a local directory to a directory on the container. So any files that are in the local directory will appear in the container directory, and vice versa.
```
export mount_dir=/Users/jongo/ml-project-starter-kit/project_files

docker run -d --rm -t -i --name ml-project-starter-kit -v $mount_dir:/src/project_files -p 8888:8888 ml-project-starter-kit:latest
```

## Access Jupyter Lab
```
http://localhost:8888
```