FROM python:3.10-slim-bullseye

# Install necessary packages for building mysqlclient
RUN apt-get update && apt-get install -y --no-install-recommends \
        build-essential \
        pkg-config \
        libmariadb-dev \
        && apt-get clean && rm -rf /var/lib/apt/lists/*

# Upgrade pip
RUN pip install --no-cache-dir --upgrade pip

# Set the working directory
WORKDIR /app

# Copy the requirements file and install Python dependencies
COPY ./requirements.txt /app
RUN pip install --no-cache-dir -r /app/requirements.txt

# Copy the entire application code
COPY . /app

# Command to run the application
CMD ["python3", "consumer.py"]

