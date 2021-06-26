# General IT Troubleshooting Guide

**Troubleshooting Guide**

```
Copyright 2021 - Abrar K

Licensed under the Creative Commons Zero v1.0 Universal (the 'License');
you may not use this file except in compliance with the License.

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an 'AS IS' BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.

See the License for the specific language governing permissions and
limitations under the License.
```

- You may obtain a copy of the license at
    [Creative Commons Zero v1.0 Universal](LICENSE)

## Table Of Contents
---
- [General IT Troubleshooting Guide](#general-it-troubleshooting-guide)
  - [## Table Of Contents](#-table-of-contents)
  - [## **Hardware**](#-hardware)
    - [**Server**](#server)
    - [**Storage**](#storage)
      - [NAS](#nas)
      - [SAN](#san)
    - [**Network**](#network)
      - [Protocol Stacks](#protocol-stacks)
      - [CRC Error](#crc-error)
  - [## **Software**](#-software)
    - [**Virtualization**](#virtualization)
      - [Ovirt](#ovirt)
      - [VMware](#vmware)
    - [**Database**](#database)
  - [## **Others**](#-others)
    - [**Fundamentals**](#fundamentals)

## **Hardware**
---

### **Server**

### **Storage**

#### NAS

#### SAN

### **Network**

#### Protocol Stacks

* OSI vs TCP/IP
  
  ![OSI and TCP/IP](attachments/OSI_TCP.png)

  - Differences between OSI and TCP/IP models

    OSI Model	| TCP/IP model
    --- | ---
    It is developed by ISO (International Standard Organization)| It is developed by ARPANET (Advanced Research Project Agency Network).
    OSI model provides a clear distinction between interfaces, services, and protocols. | TCP/IP doesn't have any clear distinguishing points between services, interfaces, and protocols.
    OSI refers to Open Systems Interconnection. | TCP refers to Transmission Control Protocol.
    OSI uses the network layer to define routing standards and protocols. | TCP/IP uses only the Internet layer.
    OSI follows a vertical approach. | TCP/IP follows a horizontal approach.
    OSI model use two separate layers physical and data link to define the functionality of the bottom layers. | TCP/IP uses only one layer (link).
    OSI layers have seven layers.	| TCP/IP has four layers.
    OSI model, the transport layer is only connection-oriented.	| A layer of the TCP/IP model is both connection-oriented and connectionless.
    In the OSI model, the data link layer and physical are separate layers.	| In TCP, physical and data link are both combined as a single host-to-network layer.
    Session and presentation layers are not a part of the TCP model.	| There is no session and presentation layer in TCP model.
    It is defined after the advent of the Internet.	| It is defined before the advent of the internet.
    The minimum size of the OSI header is 5 bytes. |	Minimum header size is 20 bytes.

  - Advantages of the TCP/IP model
      - It helps you to establish/set up a connection between different types of computers.
      - It operates independently of the operating system.
      - It supports many routing-protocols.
      - It enables the internetworking between the organizations.
      - TCP/IP model has a highly scalable client-server architecture.
      - It can be operated independently.
      - Supports a number of routing protocols.
      - It can be used to establish a connection between two computers.

   - Disadvantages of the TCP/IP model
     - TCP/IP is a complicated model to set up and manage.
     - The shallow/overhead of TCP/IP is higher-than IPX (Internetwork Packet Exchange).
     - In this, model the transport layer does not guarantee delivery of packets.
     - Replacing protocol in TCP/IP is not easy.
     - It has no clear separation from its services, interfaces, and protocols.

#### CRC Error

## **Software**
---

### **Virtualization**

#### Ovirt

#### VMware

### **Database**

## **Others**
---

### **Fundamentals**

* IT Fundamentals
  - [IT k Funde](https://www.youtube.com/channel/UC1RauiosDyz3K16X1wkaeiA)

* DevOps
  - [TechWorld with Nana](https://www.youtube.com/channel/UCdngmbVKX1Tgre699-XLlUA)