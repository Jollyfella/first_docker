# Use an official Python runtime as a parent image
FROM python:3.7-slim

# Set proxy server, replace host:port with values for your servers
ENV http_proxy 10.100.1.254:8080
ENV https_proxy 10.100.1.254:8080

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --trusted-host pypi.python.org -r requirements.txt
#RUN pip install Flask
#RUN pip install Redis

# Make port 80 available to the world outside this container
EXPOSE 80

# Define environment variable
ENV NAME World

# Run app.py when the container launches
CMD ["python", "app.py"]