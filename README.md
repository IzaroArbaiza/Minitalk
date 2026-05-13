# 📨 Minitalk

`Minitalk` is a small messaging program created as part of the 42 School curriculum. It enables inter-process communication by sending strings from client to server using UNIX signals.

## 🧠 Project Summary

- Written in **C**, using only `signal`, `kill`, and system calls  
- Implements communication via `SIGUSR1` and `SIGUSR2` signals  
- Encodes and decodes each bit of the message using signals  
- Ensures reliable delivery byte by byte  
- Complies with 42 norm and handles synchronization between processes

## 📋 Features

### ✅ Mandatory

- **Server**:  
  - Listens for incoming signals  
  - Reconstructs and prints the message once received  
  - Sends acknowledgment back to client to continue transmission

- **Client**:  
  - Sends messages to server using PID and signals  
  - Each character is sent bit by bit  
  - Waits and handles acknowledgment from server before sending next byte

## 🚀 How to Use

Clone the repository and compile:
```bash
git clone https://github.com/IzaroArbaiza/Minitalk.git
cd Minitalk && make
```

Run the server
```bash
./server
```
In another terminal, send a message via the client:
```bash
./client <server_pid> "Hello, world!"
```
