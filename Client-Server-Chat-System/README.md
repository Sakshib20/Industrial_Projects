# 💬 Client-Server Chat System (CUI)

## 📝 Project Overview
A command-line (CUI) based synchronous chat application engineered using Core Java Networking concepts. This project establishes a reliable, real-time, two-way communication channel between a client and a server over a network.

## 🚀 Key Technical Features
* **TCP/IP Socket Programming:** Utilizes Java's `ServerSocket` and `Socket` classes (from the `java.net` package) to establish a stable connection on Port `5100`.
* **Real-Time Data Streaming:** Implements `BufferedReader` and `PrintStream` (from `java.io`) to handle the continuous, real-time exchange of text messages between the client and the server.
* **Custom Handshake Protocol:** Designed a persistent connection loop where the server actively listens for incoming connection requests and maintains the session until a termination command is executed.
* **Synchronous Communication:** Ensures messages are sent and received in a strict, orderly sequence for seamless two-way chat.

## 🛠️ Technology Stack
* **Language:** Core Java
* **Core Packages:** `java.net` (Networking), `java.io` (Input/Output Streams)
* **Protocols:** TCP/IP
* **Interface:** Command Line Interface (CUI)

## ⚙️ How to Run
1. Compile both Java files: `javac ChatServerLoop.java ChatClientLoop.java`
2. Start the Server first: `java ChatServerLoop` *(It will begin listening on Port 5100)*
3. Open a new terminal and start the Client: `java ChatClientLoop`
4. Begin typing messages in either terminal to chat!