## Buld Docker Image
```
cd ml-project-starter-kit

docker build -t ml-project-starter-kit .
```

## Run Docker Contain
```
export mount_dir=/Users/jongo/ml-project-starter-kit/project_files

docker run -d --rm -t -i --name ml-project-starter-kit -v $mount_dir:/src/project_files -p 8888:8888 ml-project-starter-kit:latest
```

## Access Jupyter Lab
```
http://localhost:8888
```
