# MP3 Converter

This project is an MP3 Converter built using a microservice architecture. It allows users to upload audio files and convert them to MP3 format. The system is designed for scalability, reliability, and efficiency, implemented using microservice architecture to handle different tasks.

## Key Components

- **Flask Application** for the backend, I was gonna use fastapi so I don't have to write api documentation, but... never mind.
- **RabbitMQ** for uploading the files to the queue for making the process asynchronous and persistent in case of a system crash.
- **Kubernetes** for scaling
- **Docker** because it's cool... and also because kubernetes can't run without it.
- **MySQL & MongoDB** MySQL for storing user details and MongoDB for storing the files.
- **JWT** for obvious reasons.

## Features

- **Audio Conversion**: Supports converting various audio formats (e.g., MP4, MKV) to MP3.
- **Asynchronous Processing**: RabbitMQ enables queuing of conversion tasks, improving the user experience by offloading the work to background processes.
- **Notifications**: Users are notified when their files are ready to download, ensuring they don't need to wait for the conversion to complete in real-time.
