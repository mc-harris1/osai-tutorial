# OSaI: Learning AI Infrastructure Through the OSI Model

> A hands-on guide to AI infrastructure using NVIDIA DGX Spark systems, networking experiments, packet captures, and the OSI model to bridge classical networking with modern AI clusters.

## Overview

The Open Systems Interconnection (OSI) model has been the foundation for teaching computer networking for decades. While modern AI infrastructure has dramatically changed how systems communicate and scale, the OSI model remains an invaluable framework for understanding these systems.

**OSaI** applies the OSI model to a real AI cluster built from NVIDIA DGX Spark systems. Rather than learning networking through abstract examples, you'll build, configure, observe, and benchmark an AI infrastructure while connecting each activity back to the corresponding OSI layer.

Throughout the tutorial, you'll capture system state, inspect packet traces, measure performance, and develop an intuition for how distributed AI workloads communicate.

---

# Learning Objectives

By the end of this tutorial, you will be able to:

* Explain each OSI layer in the context of modern AI infrastructure.
* Configure networking on NVIDIA DGX Spark systems.
* Understand the role of the ConnectX-7 SmartNIC.
* Capture and analyze network traffic with Wireshark.
* Benchmark latency and throughput.
* Observe how distributed AI workloads communicate.
* Compare system state before and after infrastructure changes.
* Build a practical understanding of AI cluster networking.

---

# Intended Audience

This tutorial is intended for:

* Software Engineers
* Machine Learning Engineers
* Systems Engineers
* Platform Engineers
* DevOps Engineers
* AI Practitioners
* Students
* Technology Enthusiasts

No prior experience with AI infrastructure or high-performance computing is assumed.

---

# Hardware

## Minimum

* One NVIDIA DGX Spark
* Administrative workstation (macOS, Linux, or Windows)
* Ethernet network
* SSH access

## Recommended

* Two NVIDIA DGX Spark systems
* NVIDIA QSFP28 Direct Attach Cable
* Managed Ethernet switch
* Wireshark workstation

---

# Software

Recommended tools include:

* Git
* Visual Studio Code
* Wireshark
* iperf3
* SSH
* Docker (optional)
* NVIDIA Container Toolkit (optional)

---

# Repository Structure

```text
.
├── .github/
├── captures/
├── docs/
├── labs/
├── scripts/
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── README.md
├── ROADMAP.md
└── SECURITY.md
```

---

# Tutorial Structure

## Lab 00 — Prerequisites

Prepare the lab environment.

Topics include:

* Hardware setup
* Software installation
* Network topology
* Environment verification
* Baseline system state capture

---

## Lab 01 — Physical Layer

Understand the physical infrastructure.

Examples include:

* DGX Spark hardware
* Ethernet
* QSFP28 cabling
* ConnectX-7 interfaces
* Link verification

---

## Lab 02 — Data Link Layer

Explore Layer 2 networking.

Topics include:

* MAC addresses
* Network interfaces
* ARP
* Frame forwarding
* MTU

---

## Lab 03 — Network Layer

Configure Layer 3 networking.

Topics include:

* IPv4
* IPv6
* Routing
* Subnets
* Network configuration

---

## Lab 04 — Transport Layer

Measure communication performance.

Topics include:

* TCP
* UDP
* Latency
* Throughput
* Bandwidth testing

---

## Lab 05 — Session Layer

Examine long-lived communication between systems.

Examples include:

* SSH
* Persistent connections
* Distributed communication

---

## Lab 06 — Presentation Layer

Understand how data is represented.

Topics include:

* Serialization
* Compression
* Encryption
* Encoding

---

## Lab 07 — Application Layer

Connect networking concepts to AI software.

Examples include:

* Distributed AI frameworks
* NVIDIA software stack
* Containerized workloads
* Multi-node communication

---

# Methodology

Each lab follows a consistent structure:

1. Learning objectives
2. Background
3. Environment preparation
4. Hands-on exercises
5. Expected results
6. Validation
7. Discussion
8. Further reading

Whenever possible, experiments include:

* Before-and-after system state
* Packet captures
* Performance benchmarks
* Reproducible commands

---

# Contributing

Contributions that improve documentation, experiments, diagrams, benchmarking, and reproducibility are welcome.

Please review [CONTRIBUTING.md](CONTRIBUTING.md) before opening an issue or submitting a pull request.

---

# Roadmap

Future work includes:

* GPUDirect technologies
* BlueField DPU exploration
* Distributed inference
* Advanced networking
* Performance optimization
* Community-contributed labs

See [ROADMAP.md](ROADMAP.md) for additional details.

---

# License

This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE) file for details.

---

# Acknowledgments

This tutorial is inspired by decades of networking education built around the OSI model and by NVIDIA's continued advancement of AI infrastructure through the DGX platform, ConnectX networking, and related technologies.

