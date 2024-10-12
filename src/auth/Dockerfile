FROM python:3.10-slim-bullseye

# Install necessary packages
RUN apt-get update && apt-get install -y --no-install-recommends --no-install-suggests \
	build-essential default-libmysqlclient-dev pkg-config \
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

# Expose the application port
EXPOSE 5000

# Command to run the application
CMD ["python3", "server.py"]

