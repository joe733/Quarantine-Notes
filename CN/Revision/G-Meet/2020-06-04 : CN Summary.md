ISO / OSI Refrence model
------------------------

ISO: International Organization of Standardization
OSI: Open System Inter-connection

- 7 Layers: Physical, Data Link, Network, Transport, Session, Presnetation, Application Layer


## Principle design Fetures
- Each layes performs tasks to do a particular function
- there is an interface b/w each layer
- The function of layer must not be large nor too small.
- The lower layers communticates with the neighbouring connections only.
- Packet Data Units / Packets / Frames / Bits / Electorns / Waves

### 1. Physical Layer

> Cables / Channels

- Transmits the data at bit level / current.
- The transmitted data must be recieved without error
- Volts assigned to bits & the nanosecods it lasts
- The number of pins and cables are required.
- The devices that are used - mechanical & electical

### 2. Data Link Layer

> Swithches / Bridges

- Main task is error control.
- The packets from the network layer is converted in frames.
- These frames are then sequenced before transmission.
- The reciever confirms with ACK frams.
- Flow contorl is also done in the frame.
- Provides control access to the shared channel.
- DLL is subdived into LLC (Logical Link Contorl) & MAC (Media Access Cnontrol).
- MAC - CSMA / TDMA

### 3. Network Layer

> Routers

- This deals with the routing.
- There are algorithms to figure out routes: static & dynaamic
- Routing tables are maintained based on Logical Addressing
- Path determination: OSPF / IS-IS / 
- Another function called Conjestion Contorl (Methods like Leakybucket)
- It aims for QOS (Quality of service) e.g. Bandwidth, Jitter, time delay
- Hetrogeneous (different types & size of network) network management.

### 4. Transport layer
> Software up from here
- Accepts the data from upper layer & splits it up if needed
- Segmetation | Flow Control | Error Contorl
- Passes it to the network layer
- Ensures that it arrives correctly (true end-to-end layer)
- types of connections: error-free, point-to-point 
- Protocols : TCP (Trasmission Contorl Protocl) & UDP (User Data Protocl)

### 5. Session Layer
- Allows machines to establish sessions between machines
- Service: Dialog contorl (who's the speaker), Token Management, Synchronization
- APIS / NETBIOS
- Authentication & authorisation & Session Management

### 6. Presentation Layer
- Focues upon syntax an semantics of the information
- Encoding is done in the presentation layer
- Supports Higher lever data abstraction & data sturctures

### 7. Application Layer
- Most web application uses protocls like HTTP/S, FTP, SMTP, NNTP, DNS
- Example is a web browser which supports there protocls.