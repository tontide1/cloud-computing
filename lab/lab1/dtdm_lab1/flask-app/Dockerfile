FROM ubuntu:18.04

RUN apt-get update && apt-get install -y python3 python3-pip

# Create a working directory within the container
WORKDIR /app

COPY requirements.txt ./
RUN pip3 install --no-cache-dir -r requirements.txt

COPY app.py ./
COPY templates/index.html templates/

# Expose port number
EXPOSE 5000

# Run the application using Python 3
CMD ["python3", "app.py"]