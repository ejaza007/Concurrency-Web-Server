# Concurrent Web Server

This project involves creating a multi-threaded web server capable of handling multiple HTTP requests simultaneously. 


## Overview
This web server project showcases systems programming skills, including multi-threading, concurrency, and synchronization. The server can handle multiple client requests concurrently using a fixed-size pool of worker threads and supports different scheduling policies.

## Features
- Multi-threaded request handling
- Fixed-size request buffer
- FIFO (First-In-First-Out) scheduling
- SFF (Smallest File First) scheduling
- Synchronization using condition variables
- Security measures to prevent unauthorized file access

## Architecture
The server consists of the following components:
- **Master Thread**: Accepts new connections and places them into a fixed-size buffer.
- **Worker Threads**: Handle HTTP requests from the buffer and respond to clients.
- **Synchronization**: Achieved using condition variables to manage access to the buffer.

## Requirements
- GCC (GNU Compiler Collection)
- Make
- pthread library


