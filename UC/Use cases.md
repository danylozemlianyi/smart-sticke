## Use cases

## Revision history
|    Date    | Revision |                        Description                       |    Author    |
|:----------:|:--------:|----------------------------------------------------------|:------------:|
| 01/11/2023 |    1.0   | Initial document creation                                | Klobudsky D. |
| 02/11/2023 |    1.1   | The actor-goal list was created                          | Klobudsky D. |
| 02/11/2023 |    1.2   | The use cases were elaborated to fully-dressed use cases | Klobudsky D. |

## 1. Actor-goal list
|                       Actor                       |                                                                                                                                                                                               Goal                                                                                                                                                                                               |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Primary actor: User                               | Users aim to securely access specific rooms, devices, and resources within the enterprise using smart NFC stickers. They want to have a convenient and efficient means of entry to areas and equipment required for their job responsibilities.                                                                                                                                                  |
| Primary actor: Access control system              | The access control system's primary goal is to verify and authorize user access. It aims to provide a secure and streamlined access control process, ensuring that only authorized users with valid NFC stickers can enter specific rooms or interact with devices.                                                                                                                              |
| Supporting actor: Administrator                   | Administrators aim to efficiently manage the smart NFC sticker system. Their goals include adding and removing users, configuring access rights, creating and managing user groups, monitoring and ensuring system security, and handling administrative tasks related to the system.                                                                                                            |
| Supporting actor: Technical support               | Technical support's primary goal is to provide assistance and troubleshoot issues related to the smart NFC sticker system. Their objectives include resolving user-reported problems, ensuring system uptime, offering guidance on usage, and maintaining the system's functionality and performance. They aim to ensure a smooth user experience and address any technical challenges promptly. |
| Supporting actor: Monitoring and analytics system | The monitoring and analytics system is designed to collect and analyze data related to sticker usage and user activity. Its goals include identifying security incidents, tracking system performance, and providing insights for administrators to enhance the system's efficiency and security.                                                                                                |
| Supporting actor: Integration System              | The integration system's primary goal is to enable seamless integration of the smart NFC sticker system with other information systems within the enterprise. It aims to facilitate the exchange of data and access control information between various systems to enhance overall operational efficiency and security.                                                                          |

## 2. Use case context diagram
Figure 1: Use case context diagram for SmartSticker project

## 3. Use case model
This section includes fully dressed use cases for controlled access to specific physical objects, such as locks and electronic devices, through the use of Near Field Communication (NFC) technology.

---
| ID:                         | UC 01                                                                                                                                                                      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Use case:                   | User registration                                                                                                                                                          |
| Description:                | This use case involves the process of user registration in the system, where users provide their personal information and receive an NFC sticker for access.               |
| Level:                      | User goal                                                                                                                                                                  |
| Primary actor:              | User                                                                                                                                                                       |
| Supporting actors:          | Administrator                                                                                                                                                              |
| Stakeholders and interests: | Users aim to gain access to enterprise facilities, and administrators are responsible for managing user accounts.                                                          |
| Pre-conditions:             | The user does not have an existing account in the system.                                                                                                                  |
| Post conditions:            | The user has a registered account and an NFC sticker for access.                                                                                                           |
| Main success scenario:      | 1. The user provides their personal information to the administrator. <br> 2. The administrator creates a user account. <br> 3. The administrator issues an NFC sticker to the user. |
| Special requirements        | The user's personal information must be securely stored, and NFC stickers must be properly assigned and tracked.                                                           |
---
| ID:                         | UC 02                                                                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Use case:                   | Room access                                                                                                                                                                                          |
| Description:                | This use case involves users using their NFC stickers to gain secure access to specific rooms within the enterprise.                                                                                 |
| Level:                      | User goal                                                                                                                                                                                            |
| Primary actor:              | User                                                                                                                                                                                                 |
| Supporting actors:          | Access control system                                                                                                                                                                                |
| Stakeholders and interests: | Users seek convenient and secure room access, while the access control system ensures that only authorized users gain entry.                                                                         |
| Pre-conditions:             | The user has a valid NFC sticker.                                                                                                                                                                    |
| Post conditions:            | The user has successfully accessed the room.                                                                                                                                                         |
| Main success scenario:      | 1. The user presents their NFC sticker to the access control system. <br> 2. The access control system verifies the sticker's validity. <br> 3. The access control system grants access to the user. |
| Special requirements        | The access control system must respond quickly to grant access, and security measures should prevent unauthorized access.                                                                            |
---
| ID:                         | UC 03                                                                                                                                                                                                                 |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Use case:                   | Access rights management                                                                                                                                                                                              |
| Description:                | Administrators configure access rights for users to specific rooms and devices within the enterprise.                                                                                                                 |
| Level:                      | Administrator goal                                                                                                                                                                                                    |
| Primary actor:              | Administrator                                                                                                                                                                                                         |
| Supporting actors:          | Access control system                                                                                                                                                                                                 |
| Stakeholders and interests: | Administrators aim to efficiently manage access control, and the access control system enforces access rights.                                                                                                        |
| Pre-conditions:             | The administrator is authorized to manage access rights.                                                                                                                                                              |
| Post conditions:            | Access rights for users are configured as per the administrator's settings.                                                                                                                                           |
| Main success scenario:      | 1. The administrator accesses the access rights management interface. <br> 2. The administrator configures access rights for specific users. <br> 3. The access control system enforces the configured access rights. |
| Special requirements        | Access rights configuration must be user-friendly for administrators, and changes should take effect immediately.                                                                                                     |
---
| ID:                         | UC 04                                                                                                                                                    |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Use case:                   | Adding and removing users                                                                                                                                |
| Description:                | Administrators add new users to the system and remove users who are no longer valid.                                                                     |
| Level:                      | Administrator goal                                                                                                                                       |
| Primary actor:              | Administrator                                                                                                                                            |
| Supporting actors:          | None                                                                                                                                                     |
| Stakeholders and interests: | Administrators aim to maintain an up-to-date user list in the system.                                                                                    |
| Pre-conditions:             | The administrator has appropriate permissions.                                                                                                           |
| Post conditions:            | New users are added, or invalid users are removed from the system.                                                                                       |
| Main success scenario:      | 1. The administrator adds a new user to the system and issues an NFC sticker. <br> 2. The administrator removes an invalid user account from the system.
| Special requirements        | User addition and removal processes should be secure, and user data should be properly managed.                                                          |
---
| ID:                         | UC 05                                                                                                                                                                        |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Use case:                   | Technical support and issue resolution                                                                                                                                       |
| Description:                | Users contact technical support to resolve issues and seek assistance related to NFC stickers.                                                                               |
| Level:                      | Technical support goal                                                                                                                                                       |
| Primary actor:              | User                                                                                                                                                                         |
| Supporting actors:          | Technical support                                                                                                                                                            |
| Stakeholders and interests: | Users want prompt issue resolution and assistance, while technical support ensures a smooth user experience.                                                                 |
| Pre-conditions:             | The user encounters an issue or has a query.                                                                                                                                 |
| Post conditions:            | The user's issue is resolved, or their query is answered.                                                                                                                    |
| Main success scenario:      | 1. The user contacts technical support with their issue or query. <br> 2. Technical support assists the user in resolving the problem or provides the necessary information. |
| Special requirements        | Technical support should have the necessary knowledge and resources to resolve issues quickly.                                                                               |
---
| ID:                         | UC 06                                                                                                                                                                                                          |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Use case:                   | Monitoring and analysis of sticker usage                                                                                                                                                                       |
| Description:                | This use case involves the monitoring and analysis of NFC sticker usage to identify potential issues, track service usage, and detect unusual activities.                                                      |
| Level:                      | Monitoring and analytics system goal                                                                                                                                                                           |
| Primary actor:              | Monitoring and analytics system                                                                                                                                                                                |
| Supporting actors:          | None                                                                                                                                                                                                           |
| Stakeholders and interests: | The monitoring and analytics system aims to ensure system security and efficiency.                                                                                                                             |
| Pre-conditions:             | The system is operational and collecting usage data.                                                                                                                                                           |
| Post conditions:            | Anomalies or unusual activities are detected, and data is analyzed for system improvements.                                                                                                                    |
| Main success scenario:      | 1. The monitoring and analytics system collects NFC sticker usage data. <br> 2. The system analyzes the data to identify anomalies or patterns. <br> 3. Reports and insights are generated for administrators. |
| Special requirements        | Data collection should be continuous, and the system should have the capacity to handle large datasets.                                                                                                        |
---
| ID:                         | UC 07                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Use case:                   | Integration with other information systems                                                                                                                                                        |
| Description:                | This use case involves integrating the NFC sticker system with other information systems within the enterprise to enable data exchange and a unified access control system.                       |
| Level:                      | Integration system goal                                                                                                                                                                           |
| Primary actor:              | Integration system                                                                                                                                                                                |
| Supporting actors:          | None                                                                                                                                                                                              |
| Stakeholders and interests: | The integration system facilitates data exchange between the NFC sticker system and other systems, enhancing overall operational efficiency and security.                                         |
| Pre-conditions:             | Integration is enabled between systems.                                                                                                                                                           |
| Post conditions:            | Data is exchanged seamlessly between the NFC sticker system and other information systems.                                                                                                        |
| Main success scenario:      | 1. The integration system facilitates data exchange between the NFC sticker system and other enterprise systems. <br> 2. Data is seamlessly shared, allowing for a unified access control system. |
| Special requirements        | Integration should be robust and follow industry standards to ensure compatibility with various systems.                                                                                          |
---
