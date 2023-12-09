FROM python:3.10-slim-bullseye

# Install system dependencies
RUN apt-get update \
    && apt-get install -y --no-install-recommends --no-install-suggests \
    build-essential pkg-config ffmpeg

# Upgrade pip
RUN pip install --no-cache-dir --upgrade pip

# Set the working directory
WORKDIR /app

# Copy the requirements file and install Python dependencies
COPY ./requirements.txt /app
RUN pip install --no-cache-dir --requirement /app/requirements.txt

# Copy the rest of the application
COPY . /app

# Set the command to run the application
CMD ["python3", "consumer.py"]


