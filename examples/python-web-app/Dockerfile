# Use the official Ubuntu base image
FROM ubuntu

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements.txt and devops directory into the container at /app
COPY requirements.txt devops/ /app/

# Update packages and install Python and pip
RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip install --upgrade pip && \
    pip install -r requirements.txt

# Set the working directory for the subsequent commands
WORKDIR /app/devops

# Expose the port on which the Django app will run
EXPOSE 8000

# Command to run the Django development server
CMD ["python3", "manage.py", "runserver", "0.0.0.0:8000"]




