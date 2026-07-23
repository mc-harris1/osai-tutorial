# Lab 00 — Prerequisites

> **Objective:** Prepare a reproducible environment for the remainder of the OSaI tutorial.

---

# Overview

Before exploring AI infrastructure through the OSI model, we need to establish a reproducible environment. This lab ensures your hardware, software, and network are correctly configured and that a baseline system state has been captured.

The outputs collected in this lab will be referenced throughout the tutorial to compare how the system evolves as we introduce new networking concepts and hardware configurations.

---

# Learning Objectives

By the end of this lab, you will be able to:

* Identify the hardware used throughout the tutorial.
* Install and verify the required software tools.
* Document the physical network topology.
* Confirm connectivity to your DGX Spark system(s).
* Capture a baseline system state for future comparison.

---

# Prerequisites

You should have access to:

## Required Hardware

* One NVIDIA DGX Spark [^1]
* Administrative workstation (macOS, Linux, or Windows)
* Wi-Fi connectivity
* Administrative access to the workstation

## Recommended Hardware

* Two NVIDIA DGX Spark systems
* NVIDIA-supported QSFP direct attach cable (optional for two-node configurations)
* Managed Ethernet switch
* Internet connectivity

---

# Required Software

Install or verify the following tools on your administrative workstation.

| Tool               | Purpose               |
| ------------------ | --------------------- |
| Git                | Version control       |
| Visual Studio Code | Recommended editor    |
| Wireshark          | Packet analysis       |
| SSH client         | Remote administration |
| iperf3             | Network benchmarking  |

Optional:

* Docker
* NVIDIA Container Toolkit

---

# Lab Structure

This lab consists of five sections.

## 1. Hardware Verification

Confirm:

* DGX Spark powers on successfully.
* Ethernet cables are available.
* QSFP cable is available (if using two systems).
* Administrative workstation can communicate with the DGX Spark.

Deliverable:

* Working hardware environment.

---

## 2. Software Verification

Verify the required tools are installed on the administrative workstation.

Examples include:

* Git
* SSH
* Wireshark [^2]
* iperf3

Deliverable:

* Administrative workstation ready for future labs.

---

## 3. Network Topology

Document your current network.

Example:

```text
  MacBook
     │
   Wi-Fi
     │
Network Switch
     │
   Wi-Fi
     │
  DGX Spark
```

If using two DGX Spark systems, document both DGX Spark systems and their connectivity.

Deliverable:

* Network diagram.

---

## 4. Environment Validation

Before proceeding, verify that you can successfully access and manage your DGX Spark remotely. Remote management is required to complete the remaining labs.

NVIDIA provides multiple methods for connecting to a DGX Spark. Complete **one** of the following options:

### Option A — NVIDIA Sync (Recommended)

Follow NVIDIA's official guide to connect to your DGX Spark using NVIDIA Sync. [^3]

### Option B — Manual Remote Access

If you prefer not to use NVIDIA Sync, follow NVIDIA's documentation for manually connecting to your DGX Spark using SSH or another supported remote management method.

**Deliverable**

* Successfully establish remote access to the DGX Spark using your preferred management method.
* Verify that you can execute commands remotely.



---

## 5. Baseline System State

Capture the initial system state before introducing Ethernet or the high-speed interconnect in subsequent labs.

Suggested commands include:

```bash
hostnamectl

uname -a

ip addr

ip link

ip route

lspci

nvidia-smi
```

Save the output under:

```text
captures/
└── baseline/
```

These files will become reference points throughout the tutorial.

Deliverable:

* Baseline system-state artifacts captured under captures/baseline/.

---

# Expected Outcomes

Upon completion, you should have:

* A functioning DGX Spark environment.
* Verified remote administrative access to the system.
* Required software installed.
* A documented network topology.
* Baseline system-state captures stored in the repository.

---

# What's Next?

Continue to **Lab 01 — Physical Layer**, where you'll transition from the default Wi-Fi configuration to wired networking and begin exploring the physical infrastructure that enables AI cluster communication.


[^1]: [NVIDIA DGX Spark Initial Setup - First Boot](https://docs.nvidia.com/dgx/dgx-spark/first-boot.html)

[^2]: [LabEx Verify Wireshark Installation](https://labex.io/tutorials/wireshark-verify-wireshark-installation-548783)

[^3]: [NVIDIA Sync - Set Up Local Network Access](https://build.nvidia.com/spark/connect-to-your-spark/sync)

