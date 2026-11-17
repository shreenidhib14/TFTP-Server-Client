# TFTP Server and Client – UDP File Transfer

## Project Overview

This project implements a Trivial File Transfer Protocol (TFTP) Server and Client using C programming and UDP socket communication.

The application provides a menu-driven client interface to connect to a server and perform file upload and download operations. It uses request, data, acknowledgement, and error packets to manage file transfers between the client and server.

## Features

- UDP-based client-server communication.
- Server connection using IP address and port number.
- **RRQ (Read Request):** Download files from the server.
- **WRQ (Write Request):** Upload files to the server.
- DATA and ACK packet handling.
- Block-based data transmission.
- Timeout and retransmission handling.
- File reading and writing.
- Transfer mode selection:
  - Normal
  - Octet
  - Netascii
- Basic IP address and port validation.

## Technologies Used

- Programming Language: C
- Networking: UDP Socket Programming
- Protocol: TFTP
- Operating System: Linux
- Concepts: Client-Server Architecture, Socket Programming, File Handling, Structures, Pointers, System Calls.

## Project Structure

```text
TFTP/
│
├── TFTP.h
├── main.c
├── client.c
├── server.c
├── mode.c
│
└── server_files/
```

## Compilation

Compile the client:

```bash
gcc main.c client.c mode.c -o client
```

Compile the server:

```bash
gcc server.c mode.c -o server
```

## Execution

**Step 1: Start the server**

```bash
./server
```

**Step 2: Start the client in another terminal**

```bash
./client
```

**Step 3: Connect to the server**

Enter the server IP address:

```text
127.0.0.1
```

Enter the server port:

```text
5000
```

**Step 4: Select an operation**

```text
1. Connect
2. Put
3. Get
4. Mode (Normal/octet/Net-ascii)
5. Exit
```

- Select `Put` to upload a file.
- Select `Get` to download a file.
- Select `Mode` to choose a transfer mode.

## Key Learnings

- Understanding UDP socket programming and client-server communication.
- Implementing file upload and download operations.
- Understanding TFTP packet types and block-based data transfer.
- Working with socket APIs such as `socket()`, `bind()`, `sendto()` and `recvfrom()`.
- Implementing timeout handling and retransmission mechanisms.
- Improving knowledge of Linux system calls and network protocols.

## Author

Shreenidhi Budihal
