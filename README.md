# DPI Engine – Deep Packet Inspection System

A C++ based Deep Packet Inspection (DPI) engine that analyzes network traffic from PCAP files, classifies applications using TLS SNI extraction, applies filtering rules, and generates traffic reports.

## Features

- PCAP packet parsing
- TCP/UDP protocol analysis
- TLS SNI extraction for HTTPS traffic classification
- Flow tracking using Five-Tuple identification
- Application detection (YouTube, Facebook, Google, etc.)
- Rule-based blocking (IP, Domain, Application)
- Traffic statistics and reporting
- Multi-threaded packet processing

## Tech Stack

- C++17
- Multi-threading (`std::thread`)
- Networking Protocols (Ethernet, IPv4, TCP, UDP)
- TLS Inspection
- PCAP File Processing

## Architecture

```text
PCAP Input
    ↓
Packet Parser
    ↓
Flow Tracker
    ↓
SNI Extraction
    ↓
Traffic Classification
    ↓
Rule Engine
    ↓
Filtered PCAP + Report
```

## Key Concepts Implemented

- Deep Packet Inspection (DPI)
- Five-Tuple Flow Tracking
- TLS Client Hello Analysis
- SNI-Based Application Detection
- Producer-Consumer Architecture
- Thread-Safe Queues
- Load Balancing & Fast Path Processing

## Build

```bash
g++ -std=c++17 -pthread -O2 -I include -o dpi_engine src/*.cpp
```

## Run

```bash
./dpi_engine input.pcap output.pcap
```

Block specific applications:

```bash
./dpi_engine input.pcap output.pcap --block-app YouTube
```

## Output

- Filtered PCAP file
- Traffic statistics report
- Application breakdown
- Detected domains and applications

## Learning Outcomes

- Computer Networking
- Packet Analysis
- Protocol Parsing
- TLS/SNI Inspection
- Concurrent Programming
- High-Performance System Design
