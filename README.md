# Overview
- This repository uses socat to simulate a UART connection between OBC-Micro and OBC-AI.
- Data is transmitted between the two devices using Protobuf.

# Prerequisites 
- A C++ compiler (g++ or clang++)
- cmake and GNU Make
- A Protobuf compiler (brew install protobuf)
- socat (brew install socat)

# Creating a Virtual Serial Connection
- createVirtualPorts.sh creates two virtual serial ports, "/tmp/tty.client" and "/tmp/tty.server".

# Usage
1. Navigate to the build directory and run:
- cmake ..
- make
2. Run ./createVirtualPorts.sh
3. In a separate terminal session, navigate to build/bin/ and run ./server
4. In a separate terminal session, navigate to build/bin/ and run ./client