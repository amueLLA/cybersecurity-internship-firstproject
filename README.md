# 🔐 Cybersecurity Lab Environment Setup

A VirtualBox and Kali Linux lab for learning cybersecurity and practising authorized security testing.

## 📌 Project Overview

This project is my first lab setup task in the Networkwalks cybersecurity internship.

I configured a virtual practice environment using VirtualBox and Kali Linux, created a NAT Network, configured Kali’s IPv4 settings, and tested internet connectivity.

## 🎯 Objectives

- Run Kali Linux inside VirtualBox.
- Create a NAT Network using the subnet 10.0.0.0/24.
- Configure Kali with the address 10.0.0.2/24.
- Configure a default gateway and DNS server.
- Verify the network configuration and internet connectivity.
- Prepare the environment for future cybersecurity exercises.

## 🛠️ Tools Used

- Oracle VirtualBox
- Kali Linux
- NetworkManager
- Linux terminal commands: ip and ping

## ⚙️ Network Configuration

| Component | Configuration |
|-----------|---------------|
| Virtualization platform | Oracle VirtualBox |
| Guest operating system | Kali Linux |
| Virtual network type | NAT Network |
| Network subnet | 10.0.0.0/24 |
| Kali IPv4 method | Manual |
| Kali IPv4 address | 10.0.0.2 |
| Prefix length | /24 |
| Subnet mask | 255.255.255.0 |
| Default gateway | 10.0.0.1 |
| DNS server | 8.8.8.8 |

## 🪜 Setup Procedure

### 1. Run Kali Linux in VirtualBox

I used a Kali Linux virtual machine in VirtualBox as the foundation for the practice lab.

### 2. Configure the NAT Network

I configured a VirtualBox NAT Network with the IPv4 prefix:

10.0.0.0/24

The NAT Network provides a virtual network for the lab with outbound internet access.

### 3. Configure Kali’s IPv4 Settings

In Kali’s wired connection settings, I selected Manual and entered:

- IP address: 10.0.0.2
- Netmask: 24
- Gateway: 10.0.0.1
- DNS server: 8.8.8.8

### 4. Inspect the IP Address

I used the following command to inspect Kali’s network interfaces:

    ip addr

The terminal output showed 10.0.0.2/24 assigned to eth0.

### 5. Check the Routing Table

I checked the routing configuration using:

    ip route

The output showed a default route through 10.0.0.1.

### 6. Test Internet Connectivity

I tested connectivity to an external IP address using:

    ping -c 4 8.8.8.8
<img width="288" height="320" alt="image" src="https://github.com/user-attachments/assets/c8bb95c7-bb94-4225-ab06-4bbcca836fe2" />


## 🔎 Verification Results

| Check | Evidence | Observation |
|-------|----------|-------------|
| NAT Network subnet | VirtualBox network settings | 10.0.0.0/24 configured |
| Manual IPv4 settings | Kali connection editor | 10.0.0.2/24, gateway 10.0.0.1, DNS 8.8.8.8 entered |
| Assigned IP address | ip addr | 10.0.0.2/24 shown on eth0 |
| Default route | ip route | Default route through 10.0.0.1 |
| Internet connectivity | ping to 8.8.8.8 | Successful replies visible |


## 📸 Screenshots

### VirtualBox NAT Network

<img width="353" height="308" alt="image" src="https://github.com/user-attachments/assets/3567317a-ffcd-4ec9-a656-749c5a4774de" />


### Kali Manual IPv4 Configuration

<img width="280" height="302" alt="image" src="https://github.com/user-attachments/assets/d4379ed9-ec0b-45a3-b191-36b1dd493ff4" />


### IP Address, Routing and Connectivity Test

<img width="288" height="320" alt="image" src="https://github.com/user-attachments/assets/d3ed9f41-b3c5-4752-b7a9-fc650088eecf" />




## 💡 Learning Outcomes

This exercise helped me understand:

- How to configure a NAT Network in VirtualBox.
- How an IP address, subnet mask, gateway and DNS server work together.
- How to configure manual IPv4 settings in Kali Linux.
- How to inspect interfaces and routes using Linux commands.
- How to use ping to check connectivity.
- Why configuration screenshots and live verification results are both useful.

## 🔐 Responsible Practice

This environment is intended for cybersecurity education.
Security testing will be limited to systems I own or have explicit
permission to test.

## 🔗 Resources

- [VirtualBox](https://www.virtualbox.org/)
- [Kali Linux](https://www.kali.org/)
- Networkwalks Week 1 Project Module 1 lab instructions

## 👤 Author

**Keza Mika Samuella**

Networkwalks Cybersecurity Internship  
Week 1 — Cybersecurity and Pentesting Lab Setup
