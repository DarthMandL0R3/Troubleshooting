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
      - [Security](#security)
      - [IT Fundamentals](#it-fundamentals)
      - [DevOps](#devops)

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

* SAN - Fiber Cable CRC

  - Troubleshooting Fiber Port CRC Errors
     - For each link that sees CRC errors, document the devices and ports involved and follow each step listed below. Indicate which step corrected the problem.
     - Also document the frequency of the CRC errors incrementing in relation to the number of packet received, capture `sh stat slot/port` a couple oftimes to see if/when the CRC errors increment.
     - Interface CRC/InErrors
       - Pre-requisite:
         - Verify if the optics are Brocade Certified and are matching on both sides (SR-SR, LR-LR etc.)
         - Verify if the fiber distance is within specs for the optic.
         - Check if the optic is properly recognized by using `show media e x/y` (where x/y = slot/port).
         - During installation, clean the fiber and then connect the fiber link into the ports, A and B.
         - Check if the link light is up on both sides of the link.
         - Verify Normal operation under show optic <slot no> (no alarms).
         - If available, connect a scope to verify the power levels of the link, for each side of the link
    - If CRC errors are seen in interface statistics:
      - If the CRC errors are found to be incrementing on the port:
        - Clean the fiber end on both sides of the link.
        - If CRC errors stop, issue was dirty fiber.
        - Spray air or use optic cleaning swabs to clean the optic and reconnect the fiber
        - If CRC errors stop, issue was dirty optics
    - If CRC errors continue:
      - Reseat the optic and reconnect the link on one side
        - If CRC errors stop, issue was with the seating of this optic
    - If CRC errors continue:
      - Reseat the optic and reconnect the link on the other side
      - If CRC errors stop, issue was with the seating of this optic
        - Take the fiber strand from one side (do not move optic) and plug into a known good port and optic(A-C), if the problem continues, move to step (4)
        - If CRC errors stop, issue was with the optic or port that is no longer used (portB)
        - Replace optic in (portB) with a known good optic and return fiber stand to this (portB)
        - If errors stop it was an optic issue, or possibly a port issue
    - If CRC errors continue after moving the fiber strand from (portB) to (portC):
      - Issue is either (portA) optic, port or the issue is the fiber strand
      - Now move the other end (portA) to a known good port and optic for other end of the link (portD),if the problem continues move to step (6)
      - If CRC errors stop, issue was with the optic or port (portA)
      - Replace optic in (portA) with aknown good optic and return fiber stand to this (portA)
      - If errors stop it was an optic issue,or possibly a port issue
      - Replace fiber strand
      - If errors stop, issue was with the fiber strand
      - Move the new optics in ports (C) and (D) to the original ports (A) and (B) and connect the new fiber strand.
      - Verify whether the original ports (A) and (B) are clean without any CRC errors.
      - Put original optics back in port (A) and (B) and confirm whether the link is still clean without any CRC errors.
  - References:
    - [Huawei Guide](https://support.huawei.com/enterprise/en/doc/EDOC1100086961)
    - [IBM Guide](https://www.ibm.com/support/pages/troubleshooting-crc-errors-san)
    - [Extreme Guide](https://extremeportal.force.com/ExtrArticleDetail?an=000086714) 

<br>

* Software CRC


## **Software**
---

### **Virtualization**

#### Ovirt

#### VMware

### **Database**

## **Others**
---

### **Fundamentals**

#### Security

  - []()

#### IT Fundamentals
  - [IT k Funde](https://www.youtube.com/channel/UC1RauiosDyz3K16X1wkaeiA)

#### DevOps
  - [TechWorld with Nana](https://www.youtube.com/channel/UCdngmbVKX1Tgre699-XLlUA)