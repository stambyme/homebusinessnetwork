# Secure Home Lab for Business File Sharing

## Introduction
Welcome to my Secure Home Lab project's GitHub repository. This project showcases a specialized home network setup designed to support my personal business ISAW LLC needs, specifically for managing rental properties in Thailand and Las Vegas. This network emphasizes security, efficiency, and remote accessibility, leveraging both local and cloud-hosted technologies to enable secure file sharing and data management across continents.

## Network Overview

### Components
- **Protectli Vault with pfSense**: Acts as the primary router and firewall, ensuring network security.
- **ISP Modem**: Provides internet connectivity essential for international communication.
- **Managed Switch**: Facilitates robust connections between various network devices.
- **Raspberry Pi as NAS**: Stores and manages business files like photos, contracts, and lease agreements.
- **Wireless Access Point (AP)**: Extends Wi-Fi coverage and segregates IoT device traffic.
- **Linode Cloud Services**: Hosts Docker containers for network services and data accessibility.

### Network Map

Internet
    |
[ISP Modem]
    |
[Protectli Vault with pfSense] --- WAN
    | 
    |--- LAN --- [Managed Switch]
                  |         |
                  |         |--- [Raspberry Pi NAS]
                  |         |     (Business files for properties in Thailand and Las Vegas)
                  |         |
                  |         |--- [Wireless AP] --- Separate Wi-Fi for IoT Devices
                  |
                  |--- [Linode Cloud Services]
                           |
                           |--- [Docker Host] (Cloud-hosted)
                           |       |
                           |       |--- [Cloudflare VPN Tunnel] (Secure remote access)
                           |       |
                           |       |--- [Pi-hole and Unbound] (DNS and Ad-blocking)
                           |
                           |--- [Snort IDS] (Intrusion Detection on pfSense)


## Configuration Details

### pfSense and Protectli Vault
- **Firewall and Routing**: Central control for directing and securing traffic to ensure protected data transmission between international locations.
- **Snort IDS**: Monitors network traffic for threats, protecting sensitive business information.

### Linode Cloud Services
- **Docker Host**: Manages container that provide essential services:
  - **Cloudflare VPN Tunnel**: Facilitates secure remote access to the NAS, enabling safe file retrieval and management from anywhere.
  - **Pi-hole and Unbound**: Offers network-level ad blocking and secure DNS resolution to enhance privacy and speed.

### Business-Critical NAS
- **Function**: Provides centralized and secure data storage, accessible over the network.

### IoT Device Management
- **Wireless Network Segregation**: Uses dedicated SSIDs on the AP to keep IoT device traffic separate and secure.

## Challenges and Solutions
- **Integration Complexity**: Successfully integrated local and cloud components to work seamlessly, enhancing network functionality without compromising security.
- **Security Implementation**: Configured and fine-tuned Snort IDS on pfSense to effectively monitor and protect network traffic.

## Future Directions
- **Advanced Data Backup**: Plan to introduce more robust backup solutions to ensure data redundancy, particularly for critical business files.
- **Expand Network Monitoring**: Implement more comprehensive monitoring tools to maintain optimal network performance and security.

## Conclusion
This repository will continuously be updated as new features are integrated and improvements are made. Feedback and collaborative contributions are highly appreciated to further refine and enhance this setup.

