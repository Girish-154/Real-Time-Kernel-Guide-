
# Real-Time Kernel Installation on Ubuntu 24.04 (Using Ubuntu Pro)

## Overview

This guide explains the process of installing and enabling a Real-Time (RT) Kernel on Ubuntu 24.04 using Ubuntu Pro. A Real-Time Kernel helps reduce latency and improves system responsiveness for applications that require deterministic execution.

---

## Prerequisites

Before starting, ensure you have:

- Ubuntu 24.04 installed
- Internet connection
- Ubuntu Pro account (Free for personal use)

---

## Installation Steps

### Step 1: Verify Ubuntu Version

```bash
lsb_release -a
```
<img width="600" height="178" alt="Screenshot from 2026-07-06 09-56-34" src="https://github.com/user-attachments/assets/304e0e8e-57a4-42bb-9d9f-de7aafc66354" />

Check your Ubuntu version.

### Step 2: Update the System

```bash
sudo apt update
sudo apt upgrade -y
```

### Step 3: Install Ubuntu Pro Client

```bash
sudo apt install ubuntu-pro-client
```

Verify installation:

```bash
pro version
```

### Step 4: Get Ubuntu Pro Token

Open Ubuntu Pro Dashboard:

https://ubuntu.com/pro/dashboard

Copy your Ubuntu Pro token.

### Step 5: Attach Ubuntu Pro Account

Replace `YOUR_TOKEN` with your copied token.

```bash
sudo pro attach YOUR_TOKEN
```

Example:

```bash
sudo pro attach abc123xyz
```

### Step 6: Enable Real-Time Kernel

```bash
sudo pro enable realtime-kernel
```

### Step 7: Update Bootloader

```bash
sudo update-grub
```

### Step 8: Verify RT Kernel Package Installation

```bash
dpkg -l | grep realtime
```

### Step 9: Reboot System

```bash
sudo reboot
```

### Step 10: Verify Running Kernel

```bash
uname -a
```

Confirm that the Real-Time Kernel is active.

---


## Author

Girish
