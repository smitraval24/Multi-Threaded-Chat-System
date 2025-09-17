# Multi-Threaded Chat System

A **real-time group chat application** built with C that enables seamless communication between multiple users across a network. The system features a **concurrent server architecture** and **client applications**, providing users the ability to participate in chat rooms, exchange messages, and communicate with others instantly.

## Key Capabilities

- **Concurrent Server Design**: Manages multiple client connections at once through threading technology
- **Instant Message Exchange**: Users can transmit and receive messages without delay
- **Message Broadcasting**: Any message sent by a user is distributed to all active participants
- **Clean Exit Functionality**: Users can leave the chat cleanly by entering `"exit"`

## System Architecture

### Server Component
- Accepts incoming client connections on a designated port
- Spawns individual threads for each connected client to manage communication
- Distributes messages from any client to all other active clients

### Client Component
- Establishes connection to the server via IP address and port number
- Transmits messages to the server for distribution to all participants
- Receives messages from other participants instantly

## Technical Stack

- **Programming Language**: C
- **Network Communication**: Socket Programming APIs
- **Concurrency**: Multi-Threading Implementation

## Setup Instructions

### System Requirements
- C compiler (such as `gcc`)
- POSIX-compatible operating system (Linux, macOS, etc.)

### Installation & Execution

1. **Download the Repository**:
   ```bash
   git clone https://github.com/smitraval24/Multi-Threaded-Chat-System.git
   cd group-chat-application-c
   ```

2. **Build the Server Component**:
   ```bash
   gcc SocketServer.c -o server -lpthread
   ```

3. **Start the Server**:
   ```bash
   ./server
   ```

4. **Build the Client Component**:
   ```bash
   gcc socketclient.c -o client -lpthread
   ```

5. **Launch a Client**:
   ```bash
   ./client
   ```

6. **Add More Participants**:
   Launch additional terminal sessions and execute the client program in each.
   Begin your real-time conversation!
