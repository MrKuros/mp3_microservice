# MP3 Converter

This project is an MP3 Converter built using a microservice architecture. It allows users to upload audio files and convert them to MP3 format. The system is designed for scalability, reliability, and efficiency, integrating several components to handle different tasks.

## Key Components

- **Flask Application**: A web interface where users can upload audio files, select conversion options, and download converted MP3 files.
- **RabbitMQ**: Used for message queuing to handle file conversion tasks asynchronously. This ensures that multiple requests can be processed concurrently without overloading the system.
- **Notification System**: Users receive notifications when their file has been successfully converted and is ready for download.
- **Microservice Architecture**: The system is divided into several microservices that handle tasks such as file conversion, user authentication, and notification management, enabling easier maintenance and scalability.

## Features

- **Audio Conversion**: Supports converting various audio formats (e.g., WAV, FLAC) to MP3.
- **Asynchronous Processing**: RabbitMQ enables queuing of conversion tasks, improving the user experience by offloading the work to background processes.
- **Notifications**: Users are notified when their files are ready to download, ensuring they don't need to wait for the conversion to complete in real-time.
