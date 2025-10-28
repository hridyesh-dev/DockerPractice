# Use an official Python runtime as the base image choti image use krr raha hai
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# install required packages for system
#system update krr raha hai
RUN apt-get update \       
#system upgrade krr raha hai  
    && apt-get upgrade -y \
    #mysql ka client install krr raha hai 
    && apt-get install -y gcc default-libmysqlclient-dev pkg-config \
    && rm -rf /var/lib/apt/lists/*

# Copy the requirements file into the container
COPY requirements.txt .

# Install app dependencies
RUN pip install mysqlclient
#requirement ka code copy kiya
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY . .

# Specify the command to run your application
CMD ["python", "app.py"]

