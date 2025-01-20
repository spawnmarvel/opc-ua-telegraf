# opc-ua-telegraf
opc-ua-telegraf


### Key Differences Between OPC DA and OPC UA

OPC (OLE for Process Control) is a series of standards used in industrial automation to facilitate communication between different hardware and software components. Two of the most common specifications within the OPC suite are **OPC DA (Data Access)** and **OPC UA (Unified Architecture)**. Here's a breakdown of their differences along with an example to illustrate their usage:

### **Key Differences Between OPC DA and OPC UA**

1. **Architecture and Standards:**
   - **OPC DA:**
     - **Based On:** COM/DCOM (Component Object Model / Distributed COM) technology, which is proprietary to Microsoft.
     - **Platform Dependency:** Primarily designed for Windows environments.
     - **Communication Protocol:** Relies on COM/DCOM for communication, which can be complex to configure, especially across firewalls or different network segments.
   
   - **OPC UA:**
     - **Based On:** A service-oriented architecture that is platform-independent.
     - **Platform Independence:** Can run on various operating systems including Windows, Linux, and embedded systems.
     - **Communication Protocols:** Uses modern protocols like TCP/IP, HTTPS, and WebSockets, making it more flexible and easier to integrate across different networks and platforms.

2. **Security:**
   - **OPC DA:**
     - Limited security features, primarily relying on Windows security.
     - Vulnerable to security risks inherent in DCOM configurations.
   
   - **OPC UA:**
     - Built-in security mechanisms, including authentication, encryption, and auditing.
     - More robust against modern cybersecurity threats.

3. **Data Modeling and Information:**
   - **OPC DA:**
     - Focuses primarily on real-time data (read/write operations).
     - Limited in representing complex data structures or historical data.
   
   - **OPC UA:**
     - Supports complex data modeling, allowing for the representation of rich information structures, relationships, and hierarchies.
     - Integrates not just real-time data but also historical data, alarms, and events.

4. **Scalability and Flexibility:**
   - **OPC DA:** Better suited for simpler, single-machine setups within a Windows environment.
   - **OPC UA:** Designed to handle large-scale, distributed systems with diverse hardware and software components.

### **Example Scenario**

**Scenario:** A manufacturing plant wants to monitor and control its machinery using a supervisory control system.

- **Using OPC DA:**
  1. **OPC DA Server:** Running on a Windows-based PLC or gateway device connected to the machinery sensors and actuators.
  2. **Supervisory Application:** Also running on a Windows PC, it connects to the OPC DA server using COM/DCOM protocols to read sensor data and send control commands.
  3. **Limitations:** 
     - Both server and client need to be on Windows machines.
     - Configuring DCOM for secure and reliable communication across different network segments is complex.
     - Limited ability to extend functionalities beyond real-time data access.

- **Using OPC UA:**
  1. **OPC UA Server:** Embedded within the PLC or as a separate gateway, running on a platform of choice (Windows, Linux, etc.). It collects data from machinery sensors and manages control commands.
  2. **Supervisory Application:** Can run on various platforms (Windows, Linux, cloud-based systems) and connects to the OPC UA server using standard protocols like HTTPS.
  3. **Advantages:**
     - **Platform Flexibility:** No need for both server and client to be on Windows.
     - **Enhanced Security:** Built-in encryption and authentication ensure secure data transmission.
     - **Scalability:** Easily integrates with other systems, supports complex data models, and can handle large-scale deployments.
     - **Future-Proofing:** OPC UA is designed to accommodate future technological advancements and expanding automation needs.

### **Visual Example**

**OPC DA Setup:**
```
[PLC (Windows-based OPC DA Server)] <--COM/DCOM--> [Supervisory PC (Windows-based OPC DA Client)]
```

**OPC UA Setup:**
```
[PLC (OPC UA Server, Any Platform)]
           |
        (TCP/IP)
           |
[Supervisory System (OPC UA Client, Any Platform)]
```

### **Summary**

- **OPC DA** is suitable for straightforward, Windows-centric real-time data access scenarios but comes with limitations in platform support, security, and scalability.
  
- **OPC UA** offers a more versatile, secure, and scalable solution suitable for modern, distributed, and heterogeneous industrial environments.

For new projects or when upgrading existing systems, **OPC UA** is generally recommended due to its robustness, flexibility, and future readiness.

**Here's a table summarizing the key differences:**

| Feature          | OPC DA                         | OPC UA                            |
|-----------------|---------------------------------|------------------------------------|
| **Foundation**   | COM/DCOM                       | Platform-Independent             |
| **Platform**     | Primarily Windows                | Cross-Platform (Windows, Linux, etc.) |
| **Focus**        | Real-time Data Access          | Broader Functionality (Data, History, Alarms, Events) |
| **Security**     | DCOM Security (Complex)        | Built-in Security (Robust)        |
| **Discovery**    | Limited                        | Built-in Discovery Mechanisms     |
| **Data Encoding** | Primarily Binary               | Binary, XML, JSON                 |
| **Functionality**| Basic Data Access              | Richer Set of Services, Information Modeling |
| **Complexity**   | Can be more complex to configure | Designed for easier configuration |




## Learn OPC UA using Cogent DataHub and telegraf


### Telegraf

https://github.com/influxdata/telegraf/blob/master/plugins/inputs/opcua/README.md

### Cogent DataHub


Connect OPC UA servers and clients


https://cogentdatahub.com/features/protocols/opc-ua/


### Chapter 2. Getting Started

2.2. Test with simulated data


Documentation

https://cogentdatahub.com/library/documentation/

### Chapter 7. OPC UA Connections


Documentation

https://cogentdatahub.com/library/documentation/


