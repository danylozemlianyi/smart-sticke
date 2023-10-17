# Software Requirements Specification
## For SmartSticker

Version 0.1  
Prepared by Danylo Zemlianyi  
NaUKMA_IPZ_master_1  
16.10.2023 

Table of Contents
=================
* [Revision History](#revision-history)
* 1 [Introduction](#1-introduction)
  * 1.1 [Document Purpose](#11-document-purpose)
  * 1.2 [Product Scope](#12-product-scope)
  * 1.3 [Definitions, Acronyms and Abbreviations](#13-definitions-acronyms-and-abbreviations)
  * 1.4 [References](#14-references)
  * 1.5 [Document Overview](#15-document-overview)
* 2 [Product Overview](#2-product-overview)
  * 2.1 [Product Perspective](#21-product-perspective)
  * 2.2 [Product Functions](#22-product-functions)
  * 2.3 [Product Constraints](#23-product-constraints)
  * 2.4 [User Characteristics](#24-user-characteristics)
  * 2.5 [Apportioning of Requirements](#26-apportioning-of-requirements)
* 3 [Requirements](#3-requirements)
  * 3.1 [Functional Requirements](#31-functional-requirements)
  * 3.2 [Safety Requirements](#32-safety-requirements)
  * 3.3 [Non-Functional Requirements](#33-non-functional-requirements)
## Revision History
| Name         | Date    | Reason For Changes  | Version   |
| ------------ | ------- | ------------------- | --------- |
| D. Zemlianyi |16.10.23 |  Initial document  creation |    0.1    |


## 1. Introduction

### 1.1 Document Purpose
The purpose of this Software Requirements Specification (SRS) is to provide overview and define the requirements for the SmartSticker project. It is intended for the development team, project stakeholders, and any parties involved in the project's design and implementation.

### 1.2 Product Scope
SmartSticker is a software solution that enables controlled access to specific physical objects, such as locks and electronic devices, through the use of Near Field Communication (NFC) technology. This product allows users to interact with physical objects by scanning NFC stickers placed on these objects using a smartphone application compatible with Android OS and IOS platforms.

### 1.3 Definitions, Acronyms and Abbreviations


#### 1.3.1 Acronyms
SRS - Software Requirements Specification  
NFC - Near Field Communication  
OS - Operation System  


### 1.4 Document Overview
This document is organized into the following sections: 

- Section 1 provides document overview
- Section 2 provides a general overview of the SmartSticker project.
- Section 3 details the software requirements.

## 2. Product Overview

### 2.1 Product Perspective
SmartSticker is a product designed to provide controlled access to specific physical objects, such as locks and electronic devices, through the use of Near Field Communication (NFC) technology. It is a solution to enhance security and convenience in controlling access to physical objects.

The product's major components and their interactions can be summarized as follows:

- Smartphone Application: This component runs on Android and iOS platforms and serves as the primary interface for users. Users can scan NFC stickers affixed to objects, view object allocation status, and control objects when granted access.

- NFC Stickers: These are physical tags affixed to objects. When scanned by a user's smartphone, they transmit object identifiers to the app.

- Central Server: The app communicates with a central server that verifies user permissions for object access. The server maintains a database of users, objects, and their associated permissions.

- Physical Objects: These are the specific objects, such as locks or electronic devices, that users aim to control. They are equipped with NFC stickers.

- User Accounts: Each user has their own account within the app, which includes user profile information and access permissions.

- External Interfaces: The app interfaces with external components, including smartphones with NFC capabilities and external databases.

### 2.2 Product Functions
Product shall provide possibility to allocate specified object to a specified user and give him exclusive control on it.  

There are list of functions that system must be able to perform

- NFC Scanning: Users can scan NFC stickers affixed to physical objects using their smartphones.

- Object Identification: The product must identify the object through the transmitted identifier.

- User Accounting: system shall provide user account system to recognize specified users.

- User Verification: The product verifies whether the user has the necessary permissions to access the identified object.

- Object Allocation: If the user is granted access, the product allocates the object to that user.

- User Interaction: Users can interact with the allocated object, performing actions like open/close or turn on/turn off.

- Real-time Status: The product displays real-time status updates, allowing users to view the current allocation status of each object or/and all objects in the system.

### 2.3 Product Constraints
-  User Interfaces: The primary user interface is the mobile application running on Android and iOS smartphones. The app must provide a user-friendly and intuitive experience for scanning NFC stickers, verifying user permissions, and controlling objects, logging into user account.

- Hardware Interfaces: The product relies on the NFC technology for communication between smartphones and NFC stickers affixed to objects. Smartphone must have WI-FI interface to connect to server both local or internet.

- Software: application side of the product must be an Android and IOS applications.

### 2.4 User Characteristics
SmartSticker is designed to serve a diverse range of user classes, each with specific characteristics and requirements. Identifying and understanding these user classes is essential to tailor the product's features and functionality to meet their needs.

End Users (Consumers): 
- Frequency of Use: Regular, periodic usage depending on their access needs.
- Characteristics: Non-technical users, diverse educational backgrounds and ages, varied experience levels with NFC technology.

System Administrators:
- Frequency of Use: Regular usage for system maintenance and user management.
- Characteristics: Technical expertise, familiarity with system administration.

### 2.5 Apportioning of Requirements

NFC Scanning:
* Software Element: Mobile Application (Android and iOS)
* Description: The mobile app is responsible for scanning NFC stickers affixed to physical objects.

Object Identification:
* Software Element: Central Server and mobile application
* Description: The mobile app requests an information about the object with his NFC identifier.

User Login:
* Software Element: Central Server
* Description: The central server recieve from the application user and password pair and then send back account information for user and pairs user account to the session. The central server verifies whether the user has the necessary permissions to access the identified objects.

Object Allocation:
* Software Element: Central Server
* Description: The central server allocates the object to the user if access is granted.

User Interaction:
* Software Element: Mobile Application
* Description: The mobile app provides an interface for users to interact with the allocated object, allowing actions like open/close or turn on/turn off.


Real-time Status:
* Software Element: Mobile Application, Central Server
* Description: Both the mobile app and central server work in concert to provide real-time status updates, enabling users to view the current allocation status of each object they have access to.

## 3. Requirements

#### 3.1 Functional Requirements

| ID      | Software System | Category      | Description                        | 
|---------|-----------------|---------------|------------------------------------|
| REQ-1.1 | App            | Functional     | The application shall allow users to create accounts using username and password |
| REQ-1.2 | App            | Functional     | Users shall be able to log into app securely, with options for biometric authentication (fingerprint, face recognition) on supported devices. |
| REQ-1.3 | App            | Functional     | The application shall support NFC scanning to read and recognize the unique identifiers of SmartSticker NFC tags. |
| REQ-1.4 | App            | Functional     | Upon scanning an NFC sticker, the application shall retrieve the object identifier. |
| REQ-1.5 | App            | Functional     | The application shall provide an interface for users to view their permissions for various objects. |
| REQ-1.6 | App            | Functional     | Administrators shall be able to modify user permissions. |
| REQ-1.7 | App            | Functional     | Users with object access shall be able to control allocated objects through the application, such as locking/unlocking doors or turning devices on/off. |
| REQ-1.8 | App            | Functional     | The application shall transmit the necessary commands to the objects via the server. |
| REQ-1.9 | App            | Functional     | The application shall display the real-time status of allocated objects, indicating whether they are locked/unlocked or turned on/off. |
| REQ-1.10 | App            | Functional     | Users shall have the capability to manage their profiles, including updating personal information and changing profile pictures. |
| REQ-1.11 | App            | Functional     | The application shall use encryption and secure communication protocols to protect user data and communication with the server. |
| REQ-1.12 | App            | Functional     | The application shall be compatible with both Android and iOS platforms, adhering to the respective platform design guidelines and standards. |
| REQ-1.13 | App            | Functional     | Users shall be able to log out securely from the application, with an option to enable automatic logout after a certain period of inactivity. |
| REQ-1.14 | App            | Functional     | The application shall handle errors gracefully and display user-friendly error messages with guidance on resolving issues. |
| REQ-2.1 | Server          | Functional     | The server shall store and manage user accounts, including user registration, profile updates, and authentication. |
| REQ-2.2 | Server          | Functional     | The server shall maintain a database of objects, each with a unique identifier and associated information (e.g., object type, location). |
| REQ-2.3 | Server          | Functional     | The server shall store and manage user permissions for accessing specific objects. |
| REQ-2.4 | Server          | Functional     | Administrators shall be able to modify user permissions through the server. |
| REQ-2.5 | Server          | Functional     | The server shall track object allocations to individual users in real-time. |
| REQ-2.6 | Server          | Functional     | Object allocations and deallocations made through the application shall be reflected in the server's database. |
| REQ-2.7 | Server          | Functional     | User authentication shall be performed securely, and user actions shall be validated against their permissions. |
| REQ-2.8 | Server          | Functional     | The server shall provide a communication interface for the mobile application to send and receive data. |
| REQ-2.9 | Server          | Functional     | Data transmitted between the server and application shall use secure protocols. |
| REQ-2.10 | Server          | Functional     | The server shall maintain the real-time status of objects, reflecting changes made by users through the application. |
| REQ-2.11 | Server          | Functional     | The server shall manage user sessions, automatically logging out users after a period of inactivity for security purposes. |

### 3.2 Security Requirements

| ID       | Category     | Description                        | 
|----------|--------------|------------------------------------|
| SREQ-1 | Security     | All user accounts must require strong and unique passwords. |
| SREQ-2 | Security     | Biometric authentication (fingerprint or face recognition) should be securely implemented on supported devices. |
| SREQ-3 | Security     | Account lockout mechanisms should be in place to prevent brute force attacks. |
| SREQ-4 | Security     | Data transmitted between the application and server must be encrypted using strong encryption protocols, such as HTTPS. |
| SREQ-5 | Security     | Sensitive data, including user credentials and permissions, should be stored in the server's database using strong encryption. |
| SREQ-6 | Security     | Users should only have access to objects and features for which they have been granted explicit permissions. |
| SREQ-7 | Security     | Administrators must have the ability to assign and revoke permissions securely. |
| SREQ-8 | Security     | Communication between the application and objects (e.g., locks or electronic devices) should be encrypted and protected against unauthorized access or tampering. |
| SREQ-9 | Security     | User sessions should have a limited duration and automatically expire after a period of inactivity. |
| SREQ-10 | Security     | Logout and session termination should be implemented securely. |

### 3.3 Non-Functional Requirements

| ID       | Category     | Description                        | 
|----------|--------------|------------------------------------|
| NFREQ-1  | Non-Functional     | The system should be responsive, with a maximum response time of 2 seconds for typical user interactions. |
| NFREQ-1  | Non-Functional     | The system should be designed to scale horizontally to accommodate a growing user base and increased object allocation. |
| NFREQ-1  | Non-Functional     | The user interface should be intuitive and easy to use, requiring minimal training. |
| NFREQ-1  | Non-Functional     | The application should be compatible with a wide range of Android and iOS devices, covering multiple versions of operating systems. |
| NFREQ-1  | Non-Functional     | The application should be compatible with various screen sizes and orientations. |
