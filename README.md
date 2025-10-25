# Self-Hosted Server on Raspberry Pi 5 Using Docker

This project demonstrates the setup of a fully self-hosted server on a Raspberry Pi 5, utilizing Docker for containerization, external storage for improved performance, and Tailscale VPN for secure remote access. The system is designed to run multiple applications simultaneously, efficiently, and in a modular way, providing a personal cloud experience.

## Overview

The server uses Docker to create isolated containers for different applications. This allows easy deployment, consistent performance, and simplified management of services without conflicts. By using an external USB storage device instead of a microSD card, the system ensures faster read/write speeds, reliability, and long-term sustainability.

## Applications Hosted

1. **Pi-hole**:  
   - A network-wide ad-blocking service that filters ads for all devices connected to the local network.  
   - Customization was applied to extend the default blocklists, targeting additional IPs and domains that were not covered by universal lists.  
   - Logging and monitoring of network requests were used to identify new ad sources and update filter lists dynamically.

2. **Jellyfin**:  
   - A self-hosted media streaming server with a fully customizable interface.  
   - The front-end was customized using CSS and other tweaks to change the home screen, login screen, profile selection, and media player UI.  
   - Community feedback and contributions were used to improve performance on lower-end hardware like the Raspberry Pi, ensuring smooth media streaming.

3. **Memos**:  
   - A self-hosted journaling and notes application.  
   - Multiple instances were deployed: one for personal use and one for a small group of friends, creating a mini collaborative platform.  
   - Features such as streak tracking and personalized dashboards were utilized to enhance user experience.

## Docker Usage

- Docker provides containerization, allowing each application to run in isolation with its own dependencies.  
- This approach ensures that multiple services like Pi-hole, Jellyfin, and Memos can run on the same Raspberry Pi without interfering with each other.  
- Docker also simplifies updates, scaling, and management of these applications.  
- Cosmos OS was used as the host operating system, as it supports Docker out-of-the-box and provides network management capabilities for seamless integration with containers.  
- Docker makes it possible to experiment with multiple instances, optimize resource allocation, and maintain a clean, organized environment for each service.

## Storage Configuration

- Initially, a microSD card was used but proved unsustainable due to frequent read/write operations.  
- An external USB 3.0 drive was then used to host the operating system and Docker data, significantly improving speed, reliability, and data integrity.  
- All container volumes and persistent data are stored on this external device to prevent data loss and allow easy backups.

## Networking and Remote Access

- Tailscale VPN was set up to provide secure remote access to all services hosted on the Raspberry Pi.  
- This eliminates the need for port forwarding, reducing exposure to security risks.  
- All client devices (Mac, iPad, phone) can securely access the server over the VPN with industry-grade encryption.  
- This setup allows seamless access to Pi-hole, Jellyfin, and Memos from anywhere, as if connected locally.

## Key Highlights

- Modular and scalable deployment using Docker.  
- Customized and enhanced applications for better functionality and user experience.  
- Secure remote access using Tailscale VPN.  
- Optimized storage with an external USB drive for speed and reliability.  
- Hands-on learning of cloud-like deployment, container management, networking, and system administration.

This project demonstrates how a small-scale device like Raspberry Pi can be transformed into a multi-service, self-hosted server using Docker, providing practical experience in DevOps, cloud services, and system customization.


## Demo Images

Below are some screenshots demonstrating the setup and usage of the self-hosted Raspberry Pi server with Docker:

[demo image](https://github.com/user-attachments/assets/9399cd81-b69f-4f5c-8ff0-d9cb615e14b1)
[demo image](https://github.com/user-attachments/assets/7aa2c2e0-a384-4df2-a0b5-b99bcb443a16)
[demo image](https://github.com/user-attachments/assets/0425413f-3c40-47ff-80b3-31d3b2616c3b)
