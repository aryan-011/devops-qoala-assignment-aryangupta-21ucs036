FROM python:3.9

# FIXED - corrected path from /appp to /app
WORKDIR /app 

# FIXED - corrected filename from appy.py to app.py
COPY app.py /app

# FIXED - corrected package name from netiface to netifaces
RUN pip install flask netifaces 

# FIXED - changed "eight thousand" to 8000
EXPOSE 8000 

# FIXED - corrected command from ["pythn", "app.py"] to ["python", "app.py"]
CMD ["python", "app.py"] 
