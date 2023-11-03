# Based on the latest ubuntu
FROM ubuntu:latest

# Update APT and install Python3, Python3-pip, Flask
RUN apt-get update -y
RUN apt-get install -y python3 python3-pip
RUN pip3 install Flask
RUN pip3 install flask-cors 

# Upgrade currently installed software
RUN apt-get upgrade -y

# Create a working directory
WORKDIR /app

# Copy the python script to the working directory
COPY api.py /app

# Expose port 5252
EXPOSE 5252

# Run the Flask app
CMD ["python3", "api.py"]