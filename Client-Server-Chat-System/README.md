# 🌐 DirectLink: Real-Time Network Communication System

**DirectLink** is a high-performance, command-line (CUI) communication system engineered using **Core Java Networking** architecture. This project establishes a reliable, bi-directional synchronization channel between distributed client and server nodes over a TCP/IP network.

## 🚀 Key System Features

* **TCP/IP Socket Integration:** Utilizes `ServerSocket` and `Socket` protocols (via `java.net`) to manage stable connection handshakes on a dedicated network port (Port 5100).
* **Stream-Based Data Exchange:** Implements `BufferedReader` and `PrintStream` logic for real-time, low-latency text serialization and transmission.
* **Session Lifecycle Management:** Features a persistent connection loop where the server manages state-based listening and maintains active sessions until a termination signal is received.
* **Synchronous Network Protocol:** Ensures a strict, orderly sequence of message delivery, simulating a reliable point-to-point network bridge.

## 🛠️ Technology Stack

* **Language:** Core Java (JDK 17+)
* **Networking Layer:** `java.net` (TCP/IP Sockets)
* **Data Stream Layer:** `java.io` (Buffer Management)
* **Architecture:** Distributed Client-Server Model
* **Interface:** Command Line Interface (CUI)

## ⚙️ Deployment Instructions

1. **Compile System Modules:** `javac ChatServerLoop.java ChatClientLoop.java`
2. **Initialize Server Node:** `java ChatServerLoop` (System will start listening on Port 5100)
3. **Connect Client Node:** Open a separate terminal and execute: `java ChatClientLoop`
4. **Data Exchange:** Begin synchronous message transmission across the established network bridge.