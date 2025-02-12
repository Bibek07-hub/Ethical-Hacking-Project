# Project 1: Scanning and Enumerating a Local Network with Nmap on Kali Linux

# Introduction

In this project, we will learn how to use nmap, a powerful scanning tool, to discover devices and services running on a local network. Network scnning and enumeration are critical skills for ethical hackers,
as they help in identifying potential targets and vulnerabilities within a network. By the end of this project, you will be able to perform basic network scans, identify open ports, and gather information about
the devices on your network using Kali Linux.

# Pre-requities

* Basic understanding of network concepts (IP addresses, ports, etc.).
* familiarity with using command line interface (CLI).
* Kali Linux installed on your machine (either natively, on a virtual machine. or as a live boot).

# Lab Set-up and Tools

# Tools

* Kali Linux: A Debain-derived Linux distribution designed for digital forensics and penetration testing.
* Nmap: Network exploration tool and security/port scanner (pre-installed on kali Linux).
* A local network with multiple devices connected (Computers, printers, IoT devices, etc.).

# Installation

Nmap is pre-installed on Kali Linux. You can verify the installation or update it using the following command: 
```sh
Sudo apt-get update && sudo apt-get install nmap
```
# Tasks

# Task 1: Basic Network Scan

Step1: Open a terminal on your Kali Linux machine. 
step 2: Run a basic scan on your local network. Replace 192.168.1.0/24 with your network's IP range.
##
<tab><tab>nmap 192.168.1.0/24

Expected Output: A list of devices on your network, their IP addresses, and the open ports.

# Task 2: Scanning for Specific Ports

Step 1: To scan for specific ports (e.g., HTTP port 80), use the -p option:
##
<tab><tab>nmap -p 80 192.168.1.0/24

Expected Output: A list of devices with port 80 open.

# Task 3: Service Version Detection

Step 1: Use the -sV option to detect the version of service running on open ports:
##
<tab><tab>nmap -sV 192.168.1.0/24

Expected Output: A detailed list of open ports and the services running on them, including version information.

# Task 4: Operating System Detection

Step 1: Use the -O option to detect the operating system of devices on the network.
##
<tab><tab> sudo nmap -O 192.168.1.0/24

Expected Output: The operating system details of the devices on the network.

# Task 5: Aggressive Scan

Step 1: Perform an aggressive scan using the -A option, which includes OS detection, version detection, script scanning, and traceroute:
##
<tab><tab> sudo nmap -A 192.168.1.0/24

Extected Output: Comprehensive information about the device on the network, including open ports, services, versios, operating systems, and traceroute details.

