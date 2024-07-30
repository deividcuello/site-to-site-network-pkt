# Network Architecture Documentation

![image](https://github.com/user-attachments/assets/08461211-4e42-42d5-94ce-3c78e2fb5dc3)
![image](https://github.com/user-attachments/assets/53df976d-3ed7-4107-b2a7-7beadc764265)

This document provides a comprehensive overview of the network architecture for our multi-site setup using Cisco Packet Tracer. The network design follows the Cisco 3-tier hierarchical model and includes configurations such as VLAN, Inter-VLAN routing, DHCP Snooping, OSPF, STP, HSRP, Port Security, DNS, and NAT with dual ISP connections.

## Table of Contents
1. [Overview](#overview)
2. [Network Design](#network-design)
3. [Configuration Details](#configuration-details)
    - [VLAN and Inter-VLAN Routing](#vlan-and-inter-vlan-routing)
    - [DHCP Snooping](#dhcp-snooping)
    - [OSPF](#ospf)
    - [STP and HSRP](#stp-and-hsrp)
    - [Port Security](#port-security)
    - [DNS](#dns)
    - [NAT with Dual ISP](#nat-with-dual-isp)
4. [Site Information](#site-information)
5. [Device Access](#device-access)
6. [Images](#images)

## Overview

This document describes the network architecture and configuration for a multi-site setup using Cisco Packet Tracer. The network follows Cisco's 3-tier hierarchical design principles to ensure scalability, manageability, and reliability. The configuration includes both fundamental networking features to optimize performance and security.

## Network Design

### Cisco 3-Tier Hierarchical Model

- **Core Layer**: Provides high-speed backbone connectivity between distribution layers and to the Internet.
- **Distribution Layer**: Aggregates the access layer and provides routing between VLANs.
- **Access Layer**: Connects end devices to the network and controls access through VLANs and port security.

## Configuration Details

### VLAN and Inter-VLAN Routing

- **VLAN Configuration**: Multiple VLANs are configured to segregate network traffic and enhance security.
  - Example VLANs: VLAN 10 (HR), VLAN 20 (Finance), VLAN 30 (IT) or DEPARTMENT 1, DEPARTMENT 2, DEPARTMENT 3
- **Inter-VLAN Routing**: Enabled via Layer 3 devices in Packet Tracer to facilitate communication between different VLANs.

### DHCP Snooping

- **Purpose**: Prevents rogue DHCP servers from allocating IP addresses.
- **Configuration**: DHCP snooping is enabled on all switches to validate DHCP messages and ensure that only trusted DHCP servers can provide IP addresses.

### OSPF (Open Shortest Path First)

- **Configuration**: OSPF is used for dynamic routing between routers across sites in Packet Tracer.
  - **Router IDs**: Ensure unique router IDs are assigned.
  - **Areas**: Properly segmented into OSPF areas to optimize routing and performance.

### STP (Spanning Tree Protocol) and HSRP (Hot Standby Router Protocol)

- **STP**: Prevents network loops and ensures a loop-free topology.
  - **Root Bridge**: Configured to ensure optimal path selection.
- **HSRP**: Provides high availability by enabling multiple routers to work together as a single virtual router.
  - **Virtual IP**: Configured to ensure continuity in case of a primary router failure.

### Port Security

- **Purpose**: Protects the network from unauthorized access by limiting the number of MAC addresses per port.
- **Configuration**: Port security is enabled on all access ports with specific limits and actions on violation.

### DNS

- **DNS Configuration**: DNS services are simulated in Packet Tracer to resolve domain names to IP addresses within the network.
  - **Internal DNS**: Configured to handle internal domain resolution.
  - **External DNS**: Simulated for resolving external domain names.

### NAT with Dual ISP

- **NAT (Network Address Translation)**: Configured to allow internal IP addresses to be mapped to public IP addresses.
  - **Dual ISP Setup**: Provides redundancy and load balancing between two Internet Service Providers.
  - **Failover Mechanism**: Simulated to ensure continuous connectivity in case one ISP fails.

## Site Information

### Site 1

- **Location**: San Cristóbal, Dominican Republic
- **Devices**: 3 PCs, 4 Switches 2960-24TT, 2 Switches L3 3650-24PS, 3 Servers for DHCP, DNS and Web, 1 Router 2911.

### Site 2

- **Location**: Santo Domingo, Dominican Republic
- **Devices**: 3 PCs, 3 Switches 2960-24TT, 2 Switches L3 3650-24PS, 1 Router 2911


## Device Access

All devices in this Packet Tracer setup are secured with the following access password:

- **Password**: `cisco`

For any further assistance or to report issues, please contact the network administrator.

