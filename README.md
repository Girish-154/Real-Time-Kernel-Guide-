
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
<img width="710" height="165" alt="Screenshot from 2026-07-06 10-02-24" src="https://github.com/user-attachments/assets/813d55fd-ba32-43d7-8dcf-298eafc9f888" />


Verify installation:

```bash
pro version
```
<img width="319" height="48" alt="Screenshot from 2026-07-06 10-02-41" src="https://github.com/user-attachments/assets/35a0e8c0-5fad-4fbb-9e15-940baf3d7e06" />

### Step 4: Get Ubuntu Pro Token

Open Ubuntu Pro Dashboard:

https://ubuntu.com/pro/dashboard

Copy your Ubuntu Pro token.

### Step 5: Attach Ubuntu Pro Account

Replace `YOUR_TOKEN` with your copied token.

```bash
sudo pro attach YOUR_TOKEN
```

<img width="416" height="50" alt="Screenshot from 2026-07-06 10-05-25" src="https://github.com/user-attachments/assets/08a98218-1457-42eb-bcf8-eb26831e6f36" />


### Step 6: Enable Real-Time Kernel

```bash
sudo pro enable realtime-kernel
```
<img width="903" height="361" alt="Screenshot from 2026-07-06 10-22-32" src="https://github.com/user-attachments/assets/18e86fe4-11a1-4c28-805f-e9a4761d891d" />

### Step 7: Enable Real-Time Kernel

```bash
sudo pro enable realtime-kernel
```
<img width="903" height="361" alt="Screenshot from 2026-07-06 10-22-32" src="https://github.com/user-attachments/assets/18e86fe4-11a1-4c28-805f-e9a4761d891d" />

### Step 8: Update Bootloader

```bash
sudo update-grub
```
<img width="874" height="318" alt="Screenshot from 2026-07-06 10-23-13" src="https://github.com/user-attachments/assets/bf7cd64c-7bc4-4057-b90d-cbd4240b10e5" />

### Step 9: Verify RT Kernel Package Installation

```bash
dpkg -l | grep realtime
```
<img width="876" height="377" alt="Screenshot from 2026-07-06 10-23-40" src="https://github.com/user-attachments/assets/e4b13683-54da-43db-90b9-15b1314db1e6" />

### Step 10: Reboot System

```bash
sudo reboot
```

### Step 11: Verify Running Kernel

```bash
uname -a
```
<img width="814" height="80" alt="Screenshot from 2026-07-06 11-10-13" src="https://github.com/user-attachments/assets/eee11fb1-637f-45e1-bd9f-8b75a0a93912" />

Confirm that the Real-Time Kernel is active.

---
