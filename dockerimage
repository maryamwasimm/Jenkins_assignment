# Use an official Python runtime as the base image
FROM python:3.9

# Set the working directory in the container
WORKDIR /var/jenkins_home/workspace/Assignment1-final@2


# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Make port 80 available to the world outside this container
EXPOSE 80

# Run app.py when the container launches
CMD ["python", "calc.py"]
