# Overview
This repository demonstrates how to use **socat** to simulate a UART connection between the OBC-Micro and OBC-AI devices. All data is transmitted using Protobuf for streamlined serialization and deserialization.

---

## Prerequisites
Make sure the following are installed:
- A C++ compiler (e.g., `g++` or `clang++`)
- `cmake` and GNU Make
- Protobuf compiler (e.g., `brew install protobuf`)
- `socat` (e.g., `brew install socat`)

---

## Creating a Virtual Serial Connection
The script `createVirtualPorts.sh` creates two virtual serial ports, `/tmp/tty.client` and `/tmp/tty.server`, simulating a UART connection between the two devices.

---

## Usage
1. From the **build** directory, run:
   ```bash
   cmake ..
   make
   ```
2. Execute the following script to create the virtual ports:
   ```bash
   ./createVirtualPorts.sh
   ```
3. In a separate terminal, go to `build/bin/` and run:
   ```bash
   ./server
   ```
4. In another terminal, go to `build/bin/` and run:
   ```bash
   ./client
   ```