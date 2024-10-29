# FIXED - corrected "nginx:latests" to "nginx:latest"
FROM nginx:latest 

# FIXED - corrected filename from "nginix.conf" to "nginx.conf"
COPY nginx.conf /etc/nginx/nginx.conf 

# ADDED - Copying HTML files to the correct location
# FIXED - corrected destination directory from "htmll" to "html"
# REMOVED - unwanted line
# COPY ./html /usr/share/nginx/html 

# FIXED - changed "eighty" to 80
EXPOSE 80 


# FIXED - corrected "daemon of;" to "daemon off;"
CMD ["nginx", "-g", "daemon off;"] 
