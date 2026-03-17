# 🔒 SecurePack: Industrial Data Integrity & Archival System

**SecurePack** is a Java-based security utility engineered for high-performance data aggregation and secure archival. It focuses on maintaining **System Security** by packing distributed files into an authenticated, encrypted archive while preserving critical metadata.

## 🚀 Key Security & System Features

* **Advanced Data Integrity:** Implements **MD5 Checksum** validation to ensure zero bit-loss and verify data consistency during the transmission lifecycle.
* **Authentication Layer:** Integrated **Magic Number** verification to authenticate archive headers, preventing unauthorized system access or data injection.
* **Metadata Orchestration:** Automatically preserves file attributes, headers, and exact byte-offsets within a custom-defined system architecture.
* **Encrypted Serialization:** Securely packs entire directory structures into encrypted byte-streams, optimizing storage and ensuring secure data transport.

## 🛠️ Technology Stack

* **Language:** Core Java (JDK 17+)
* **Security Integration:** MD5 Hashing, Magic Number Authentication, Custom Encryption
* **Core Systems:** Java File I/O, Byte Stream Manipulation, RandomAccessFile
* **Interface:** Command-Line Interface (CUI)

## ⚙️ Deployment & Execution

1. **Build Module:** `javac Packer.java Unpacker.java`
2. **System Aggregation (Pack):** `java Packer <Directory_Path> <Archive_Name>`
3. **System Extraction (Unpack):** `java Unpacker <Archive_Name>`
4. **Verification:** The system automatically executes a checksum validation to ensure archive integrity before extraction.