# University Campus Network Security
## Implementation of Network Security Mechanisms Using Cisco Packet Tracer

A university campus network security project implemented using Cisco Packet Tracer. This project focuses on protecting a simulated campus network against unauthorized access through multiple security mechanisms, including MAC filtering, RADIUS authentication, Access Control Lists (ACLs), switch port security, and secure router access.

The network consists of four main areas: Wireless, Wired Lab, Library, and Administration.

## Table of Contents

- [Introduction](#introduction)
- [Security Issues and Requirements](#security-issues-and-requirements)
- [Network Design](#network-design)
- [Security Tools and Mechanisms](#security-tools-and-mechanisms)
- [Implementation Steps](#implementation-steps)
  - [Step 1: Network Topology](#step-1-network-topology)
  - [Step 2: Basic Router Configuration](#step-2-basic-router-configuration)
  - [Step 3: End Device Configuration](#step-3-end-device-configuration)
  - [Step 4: RADIUS Server Configuration](#step-4-radius-server-configuration)
  - [Step 5: Wireless Router Configuration](#step-5-wireless-router-configuration)
  - [Step 6: Secure Router Access](#step-6-secure-router-access)
  - [Step 7: Configure AAA and RADIUS Authentication](#step-7-configure-aaa-and-radius-authentication)
  - [Step 8: Configure ACL](#step-8-configure-acl)
  - [Step 9: Configure MAC Filtering](#step-9-configure-mac-filtering)
  - [Step 10: Configure Switch Port Security](#step-10-configure-switch-port-security)
- [Testing and Results](#testing-and-results)
- [Project Files](#project-files)
- [How to Open the Project](#how-to-open-the-project)
- [Conclusion](#conclusion)


## Introduction

Modern campus networks face multiple security threats, including unauthorized access, data breaches, and misuse of network resources.

This project presents a simulated university campus network designed using Cisco Packet Tracer. The network is divided into four areas, each with specific security requirements:

- Wireless Area
- Wired Lab
- Library Area
- Administration Area

The main objective is to secure the campus network against unauthorized access while maintaining normal connectivity for legitimate users.

## Security Issues and Requirements

### Security Issues

- Unauthorized devices connecting to Wi-Fi.
- Users accessing restricted systems.
- Lack of centralized authentication.
- Insider threats within the network.
- Unauthorized physical connections to switches.
- Unauthorized access to critical servers.

### Security Requirements

- Restrict wireless access to authorized devices.
- Authenticate users before granting network access.
- Prevent unauthorized physical connections.
- Protect critical servers, including the Library Server and Campus Server.
- Restrict access to sensitive network resources.
- Secure network devices against unauthorized configuration access.

## Network Design

The campus network consists of four main areas:

| Network Area | Description |
|---|---|
| Wireless Area | Provides wireless connectivity for authorized laptops and users. |
| Wired Lab | Contains wired PCs with controlled access to network resources. |
| Library Area | Contains the Library Admin PC and Library Server, protected using access restrictions and port security. |
| Administration Area | Contains the Admin PC and RADIUS Server for centralized authentication. |

### Network Topology Overview

The following figure shows the overall network design and the connected devices.

![Figure 1 - Network Topology Overview](Figure%201%20Network%20Topology%20Overview.png)

## Security Tools and Mechanisms

The project uses the following security mechanisms:

| Security Mechanism | Purpose |
|---|---|
| Secure Device Access | Protects router configuration and privileged access. |
| RADIUS Authentication | Provides centralized username and password authentication. |
| Switch Port Security | Prevents unauthorized physical devices from connecting to switches. |
| Access Control Lists (ACLs) | Restricts network traffic based on IP addresses. |
| MAC Filtering | Allows only authorized wireless devices to connect. |

# Implementation Steps

## Step 1: Network Topology

The first step is to build the campus network topology in Cisco Packet Tracer.

The topology includes:

- One router as the core gateway.
- One switch for LAN connectivity and port security.
- One wireless router for wireless access.
- One server for RADIUS authentication.
- Multiple PCs and laptops representing users in different campus areas.

Refer to Figure 1 for the complete network topology.

## Step 2: Basic Router Configuration

Configure the router with the required basic network settings and interfaces to support communication between the campus network areas.

![Figure 2 - Basic Router Configuration](Figure%202%20Basic%20Router%20Configuration.png)

## Step 3: End Device Configuration

Configure the network devices with their required IP addressing and network settings.

### 3.1 PC0 Configuration – Wired Lab

![Figure 3 - PC0 Configurations (Wired Lab)](Figure%203%20PC0%20Configurations%20%28Wired%20Lab%29.png)

### 3.2 Library Admin PC Configuration

![Figure 4 - Library Admin PC Configurations](Figure%204%20Library%20Admin%20PC%20configurations%20%28Library%20Area%29.png)

### 3.3 Library Server Configuration

![Figure 5 - Library Server Configurations](Figure%205%20Library%20Server%20Configurations%20%28Library%20Area%29.png)

### 3.4 Laptop1 Configuration – Wireless Area

![Figure 6 - Laptop1 Configurations](Figure%206%20Laptop1%20Configurations%20%28Wireless%20Area%29.png)

### 3.5 Admin PC Configuration – Administration Area

![Figure 7 - Admin PC Configurations](Figure%207%20Admin%20PC%20Configurations%20%28Administration%20Area%29.png)

## Step 4: RADIUS Server Configuration

Configure the RADIUS server in the Administration Area.

The server provides centralized authentication using usernames and passwords for supported network access.

![Figure 8 - RADIUS Server Configurations](Figure%208%20RADIUS%20Server%20Configurations%20%28Administration%20Area%29.png)

## Step 5: Wireless Router Configuration

Configure the wireless router to support wireless connectivity and the required authentication settings.

### 5.1 Internet Setup

![Figure 9 - Wireless Router Internet Setup](Figure%209%20Wireless%20Router%20Configuration%20%28Internet%20Setup%29.png)

### 5.2 Network Setup

![Figure 10 - Wireless Router Network Setup](Figure%2010%20Wireless%20Router%20Configuration%20%28Network%20Setup%29.png)

## Step 6: Secure Router Access

Protect the router against unauthorized configuration access.

### 6.1 Secure Privileged Mode

Configure an enable secret password to protect privileged EXEC mode.

![Figure 11 - Secure Router Privileged Mode](Figure%2011%20Secure%20the%20Router%20Privileged%20mode.png)

### 6.2 Secure Router Remote Access

Configure and test remote access authentication.

The supplied implementation screenshot documents remote access via Telnet.

![Figure 12 - Secure Router Remote Access via Telnet](Figure%2012%20Secure%20Router%20Remote%20Access%20%28Via%20Telnet%29.png)

### 6.3 Configure Username and Password

Configure a local username and password to require authentication before accessing the router.

![Figure 13 - Secure Router via Username and Password](Figure%2013%20Secure%20Router%20Via%20Username%20and%20Password.png)

## Step 7: Configure AAA and RADIUS Authentication

### 7.1 Configure RADIUS User Credentials

Configure usernames and passwords on the RADIUS server for authentication.

![Figure 14 - RADIUS Server Username and Password](Figure%2014%20RADIUS%20Server%20configuration%20%28username-password%29.png)

### 7.2 Configure AAA Authentication

Configure AAA authentication using the RADIUS server on the wireless router.

This allows the wireless network to authenticate users using their individual credentials.

![Figure 15 - AAA Authentication Using RADIUS](Figure%2015%20Configuring%20AAA%20authentication%20using%20RADIUS%20server%20on%20wireless%20router.png)

## Step 8: Configure Access Control Lists (ACLs)

Configure ACL rules to control network traffic based on IP addresses.

The ACL is used to restrict a specific PC from accessing protected network resources while allowing authorized devices.

![Figure 16 - Configuring ACL](Figure%2016%20Configuring%20ACL%20to%20restrict%20access%20for%20specific%20PC.png)

## Step 9: Configure MAC Filtering

Apply MAC address filtering on the wireless router.

The filtering configuration allows authorized wireless devices while preventing unauthorized laptops from connecting.

![Figure 17 - MAC Address Filtering](Figure%2017%20Applying%20MAC%20address%20filtering%20on%20wireless%20router.png)

## Step 10: Configure Switch Port Security

Configure port security on the Library switch to restrict the devices allowed to connect to its ports.

The configuration uses MAC address restrictions to prevent unauthorized physical connections.

![Figure 18 - Port Security on Library Switch](Figure%2018%20Configuring%20port%20security%20on%20library%20switch.png)

# Testing and Results

After implementing the security mechanisms, several tests were performed to verify that unauthorized access was restricted while authorized users maintained normal network connectivity.

## 1. Privileged Mode Access Verification

The router privileged mode protection was tested to verify that authentication is required.

![Figure 19 - Privileged Mode Access Verification](Figure%2019%20Privileged%20Mode%20Access%20Verification.png)

## 2. Router Remote Access Authentication

The router requires authentication before allowing remote access.

![Figure 20 - Router Remote Access Authentication](Figure%2020%20Router%20requires%20authentication%20before%20remote%20access..png)

## 3. Successful RADIUS Authentication

The RADIUS authentication test demonstrates successful authentication using valid user credentials.

![Figure 21 - Successful RADIUS Authentication](Figure%2021%20Successful%20RADIUS%20Authentication.png)

## 4. ACL Verification

The ACL successfully blocks PC0 while allowing PC1 to access the Library network.

![Figure 22 - ACL Verification](Figure%2022%20PC0%20is%20blocked%20by%20ACL%20while%20PC1%20is%20allowed%20access%20to%20the%20library%20network..png)

## 5. MAC Filtering Verification

The wireless router blocks an unauthorized laptop while allowing an authorized device to connect to the wireless network.

![Figure 23 - MAC Filtering Verification](Figure%2023%20MAC%20filtering%20blocks%20unauthorized%20laptop%20while%20allowing%20authorized%20device%20to%20connect%20to%20the%20wireless%20network..png)

## 6. Authorized Library Devices

Authorized devices maintain normal network access in the Library Area.

![Figure 24 - Authorized Library Devices](Figure%2024%20Library%20authorized%20devices%20maintain%20normal%20network%20access.png)

## 7. Port Security Verification

The Library switch successfully blocks an unauthorized device attempting to connect to the network.

![Figure 25 - Port Security Verification](Figure%2025%20Port%20security%20successfully%20blocking%20unauthorized%20device%20in%20library%20area.png)

## Results Summary

| Test | Expected Result | Result |
|---|---|---|
| Privileged mode protection | Require authentication | Verified |
| Router remote access | Require login credentials | Verified |
| RADIUS authentication | Accept valid credentials | Successful |
| ACL restriction | Block PC0 and allow PC1 | Verified |
| MAC filtering | Block unauthorized laptop | Verified |
| Library connectivity | Authorized devices retain access | Verified |
| Switch port security | Block unauthorized device | Verified |

# Project Files

The repository contains the Cisco Packet Tracer project and screenshots documenting the implementation and testing.

| File | Description |
|---|---|
| `Project.pkt` | Complete Cisco Packet Tracer project file |
| Figures 1–18 | Network topology and security configuration screenshots |
| Figures 19–25 | Security testing and verification screenshots |


# Conclusion

The project successfully implemented multiple network security mechanisms to protect a simulated university campus network.

By combining MAC filtering, RADIUS authentication, ACLs, switch port security, and secure router access, different types of security threats were addressed across the Wireless, Wired Lab, Library, and Administration areas.

The testing results demonstrate that unauthorized access can be restricted while legitimate users and devices maintain normal network connectivity.

This project demonstrates how layered network security mechanisms can be designed, configured, and tested using Cisco Packet Tracer.



---

*Academic Network Security Project – University Campus Network Security Implementation.*
