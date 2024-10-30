# Qoala Assignment Report

## Final Output
![Application Running](./RunningAppn.png)
![Logs](./logs.png)

### AWS Instance Link(only http request supported)
<a href="http://ec2-13-61-3-53.eu-north-1.compute.amazonaws.com/" target="_blank">Access the AWS Instance Here</a> 


## Issues Identified
During the image building and container setup for the Nginx and Python applications, the following errors were encountered:
- Nginx configuration errors due to typos and incorrect directives.
- Dockerfile errors including obsolete attributes and incorrect command syntax.
- Issues with port definitions and missing files that prevented the applications from running correctly.

## Resolution Steps
To resolve the identified issues, the following actions were taken:

### Nginx Dockerfile Changes (`nginx/Dockerfile`)
1. **Base Image**: Changed from `FROM nginx:latests` to `FROM nginx:latest`.
2. **Configuration File**: Corrected the COPY command from `COPY nginix.conf /etc/nginx/nginx.conf` to `COPY nginx.conf /etc/nginx/nginx.conf`.
3. **Port Exposure**: Fixed port definition from `EXPOSE "eighty"` to `EXPOSE 80`.
4. **HTML Directory Copy**: Removed erroneous copy command and ensured the destination was correctly specified.
5. **Run Command**: Updated the command from `CMD ["nginx", "-g", "daemon of;"]` to `CMD ["nginx", "-g", "daemon off;"]`.

### Nginx Configuration File Changes (`nginx/nginx.conf`)
1. Corrected `worker_process` to `worker_processes`.
2. Fixed `worker_connection` to `worker_connections`.
3. Changed `include /etc/nginx/mime.typess` to `include /etc/nginx/mime.types`.
4. Updated `default_typ` to `default_type`.

### Python Application Changes (`Python/app.py`)
- Removed unused import `import socket`.

### Python Dockerfile Changes (`Python/Dockerfile`)
1. Updated the base image to `FROM python:3.9`.
2. Corrected working directory from `WORKDIR /appp` to `WORKDIR /app`.
3. Fixed the application file copy from `COPY appy.py /app` to `COPY app.py /app`.
4. Corrected package installation command from `RUN pip install flask netiface` to `RUN pip install flask netifaces`.
5. Fixed port exposure from `EXPOSE "eight thousand"` to `EXPOSE 8000`.
6. Updated the run command from `CMD ["pythn", "app.py"]` to `CMD ["python", "app.py"]`.

### Summary
These updates have improved the functionality and accuracy of the Docker configurations and application logic. All changes in the individual files have been thoroughly commented for clarity.
