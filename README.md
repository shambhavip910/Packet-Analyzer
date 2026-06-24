# Packet Analyzer

A C++ network packet analysis tool that reads PCAP files and extracts detailed information from Ethernet, IPv4, TCP, and UDP packets. The project provides packet-level visibility into network traffic by parsing protocol headers and displaying packet metadata in a human-readable format.

## Architecture

```text
PCAP File
    │
    ▼
PCAP Reader
    │
    ▼
Packet Parser
    │
    ▼
Ethernet Frame Analysis
    │
    ▼
IPv4 Packet Analysis
    │
    ▼
TCP / UDP Header Analysis
    │
    ▼
Packet Summary Output
```

## Features

* Read and process PCAP files
* Parse Ethernet frames
* Analyze IPv4 packet headers
* Inspect TCP packet information
* Inspect UDP packet information
* Extract source and destination IP addresses
* Extract source and destination ports
* Display TCP flags and sequence information
* View packet payload previews
* Generate packet-level traffic summaries

## Technologies Used

* C++
* TCP/IP Networking
* Ethernet Protocol Analysis
* Packet Parsing
* PCAP Processing
* CMake

## Project Structure

```text
include/
├── packet_parser.h
├── pcap_reader.h
└── types.h

src/
├── main.cpp
├── packet_parser.cpp
└── pcap_reader.cpp
```

## Build

```bash
mkdir build
cd build
cmake ..
cmake --build . --config Release
```

## Run

```bash
packet_analyzer input.pcap
```

Example:

```bash
packet_analyzer capture.pcap
```

## Learning Outcomes

* Network packet structure
* Ethernet frame parsing
* IPv4 header analysis
* TCP and UDP protocol inspection
* PCAP file processing
* Network traffic analysis fundamentals
