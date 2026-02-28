# 🗜️ File Packer & Unpacker With Encryption

A command-line Java utility that merges multiple files into a single encrypted archive to save disk space and transport data efficiently, complete with a dedicated extraction module.

## 🚀 Core Features
* **Pack & Extract:** Combine an entire directory of files into one custom archive, and extract them back to their original state.
* **Metadata Intact:** Automatically preserves original file names and exact byte sizes inside a custom file header.
* **Highly Secure:** Encrypts file data during packing and validates data integrity using **MD5 Checksums** and **Magic Number** authentication before unpacking.

## 🛠️ Tech Stack
* **Language:** Core Java
* **Interface:** Command-Line (CUI)
* **Core Concepts:** File I/O, Byte Streams, Cryptography, Hashing
