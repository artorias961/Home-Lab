
# Home Lab
<img width="1623" height="1005" alt="image" src="https://github.com/user-attachments/assets/ba886b55-731c-4bc3-9334-f4e413c90b98" />

## Overview

This project is a long-term home infrastructure and automation system designed to support real family needs.
It is something I wanted to build when I was younger but could not afford or maintain properly at the time.
Now that I have a stable engineering job and I am saving responsibly, I am building this system carefully and intentionally.

The goal is **stress reduction, safety, and reliability** — not flashy consumer IoT.

As my parents get older, small things like forgetting whether a door is open, a light is on, or the thermostat is set correctly can create unnecessary stress.  
This system quietly handles those concerns in the background while preserving privacy and control.



## Core Goals

- Reduce daily stress for my parents
- Improve home safety and awareness
- Maintain privacy with a local-first design
- Build a modular, maintainable system
- Allow future expansion as family needs evolve



## High-Level Architecture

### Network Layer
- ISP Fiber → ONT → Custom Network Gateway
- Managed network switch as the backbone
- Mesh routers for whole-home Wi-Fi coverage
- Network segmentation (VLANs) for isolation and security

### Security & Gateway
- Local firewall and routing
- DNS filtering (e.g., ad/malware blocking)
- VPN for secure remote access
- No cloud dependency for core functionality

### Compute & Virtualization
- Proxmox as the virtualization host
- Linux virtual machines (Ubuntu Server)
- Containerized services for isolation and reliability

### Core Services
- Home Assistant for automation and monitoring
- Media services (e.g., Jellyfin)
- Secrets management (Vault / password services)
- System monitoring and logging

### IoT & Edge Devices
- ESP32-based sensors (doors, power usage, environment)
- Smart displays (e.g., Magic Mirror)
- Local communication where possible

### Storage & Backups
- NAS with ZFS / RAID
- Automated VM and data backups
- Redundancy to avoid single points of failure



## Design Philosophy

- **Local-first**: Core services run locally without cloud dependency  
- **Privacy-aware**: Sensitive network details remain private  
- **Modular**: Services can be replaced or upgraded independently  
- **Family-oriented**: Technology should reduce stress, not add complexity  



## Public vs Private Repository Structure

### Public Branch
- High-level architecture diagrams
- Non-sensitive configuration examples
- Lessons learned and documentation
- General setup guidance

### Private Branch
- Network topology details
- Credentials and secrets
- Internal IP addressing and VLAN structure
- Security-sensitive artifacts

This approach allows transparency and learning without compromising security.



## Project Status

This project is **actively evolving**.
Components and services will be added, removed, or refined as requirements change.
The focus is long-term reliability rather than rushing features.


