## Solution to the Qoala Assignment

### Nginx Dockerfile Changes (`nginx/Dockerfile`)
- **Base Image**: 
  - **Updated**: `FROM nginx:latests` 
  - **To**: `FROM nginx:latest`
  
- **Configuration File**: 
  - **Updated**: `COPY nginix.conf /etc/nginx/nginx.conf`
  - **To**: `COPY nginx.conf /etc/nginx/nginx.conf`
  
- **Port Exposure**: 
  - **Updated**: `EXPOSE "eighty"`
  - **To**: `EXPOSE 80`

- **HTML Directory Copy**: 
  - **Removed**: `COPY ./html /usr/share/nginx/html`
  - **Updated**: Changed the destination from `htmll` to `html`.

- **Run Command**: 
  - **Updated**: `CMD ["nginx", "-g", "daemon of;"]`
  - **To**: `CMD ["nginx", "-g", "daemon off;"]`

### Nginx Configuration File Changes (`nginx/nginx.conf`)
- **Worker Processes**: 
  - **Updated**: `worker_process` 
  - **To**: `worker_processes`

- **Worker Connections**: 
  - **Updated**: `worker_connection`
  - **To**: `worker_connections`

- **MIME Types**: 
  - **Updated**: `include /etc/nginx/mime.typess`
  - **To**: `include /etc/nginx/mime.types`

- **Default Type**: 
  - **Updated**: `default_typ`
  - **To**: `default_type`

### Python Application Changes (`Python/app.py`)
- **Import Statement**: 
  - **Removed**: Unused import `import socket`.

### Python Dockerfile Changes (`Python/Dockerfile`)
- **Base Image**: 
  - **Updated**: `FROM python:3.9`
  
- **Working Directory**: 
  - **Updated**: `WORKDIR /appp`
  - **To**: `WORKDIR /app` # fixed typo

- **Copy Application File**: 
  - **Updated**: `COPY appy.py /app`
  - **To**: `COPY app.py /app` # fixed filename

- **Package Installation**: 
  - **Updated**: `RUN pip install flask netiface`
  - **To**: `RUN pip install flask netifaces` # fixed package name

- **Port Exposure**: 
  - **Updated**: `EXPOSE "eight thousand"`
  - **To**: `EXPOSE 8000` # fixed port definition

- **Run Command**: 
  - **Updated**: `CMD ["pythn", "app.py"]`
  - **To**: `CMD ["python", "app.py"]` # fixed command

### Summary
These updates improve the functionality and accuracy of the Docker configurations and application logic.

### Individual File Comments
All changes in the individual files are thoroughly commented for clarity. 

## Final Output

![Application Running](./RunningAppn.png)
![Logs](./logs.png)
