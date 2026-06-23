
# 🖥️ Simple Operating System Simulation

## 📖 Overview
This assignment simulates the core components of a simple Operating System (OS) to demonstrate the fundamental concepts of CPU scheduling, process synchronization, and memory management. 

The simulated OS manages two primary virtual resources—**CPU(s)** and **RAM**—allowing multiple user-created processes to share and utilize computing resources efficiently.

## 🎯 Project Goals
The main objective of this assignment is to understand the principles of a simple OS by designing and implementing its key modules:
* **CPU Scheduler & Dispatcher:** Determines which process is allowed to run on which CPU.
* **Process Synchronization:** Ensures coordinated execution of concurrent processes.
* **Virtual Memory Engine:** Manages memory allocation from virtual to physical memory, isolating the memory space of each process.

## ⚙️ Core Architecture
The system architecture revolves around two core engines:
1.  **Scheduler Module:** Manages the lifecycle and execution queues of processes.
2.  **Memory Management Unit (MMU):** Uses a Paging-based mechanism to map and translate virtual addresses provided by processes into corresponding physical addresses in the shared RAM.

## 📂 Source Code Structure
The repository is organized into headers, source files, and I/O directories for verification.

### 📁 Headers (`.h`)
* **Core Systems:** `common.h` (shared structs/functions), `timer.h` (system timer), `cpu.h` (virtual CPU operations), `bitopts.h` (bit operations).
* **Scheduling:** `queue.h` (PCB queues), `sched.h` (scheduler functions).
* **Memory Management:** `os-mm.h`, `mm.h` (Paging-based memory management structures).
* *Legacy/Optional:* `loader.h` (obsoleted loader), `mem.h` (obsoleted VM engine), `os-cfg.h` (optional software config switches).

### 📄 Source Files (`.c`)
* **Main Entry:** `os.c` (Starts the OS system).
* **Core Systems:** `timer.c`, `cpu.c`, `loader.c` (loads programs from disk to memory).
* **Scheduling:** `queue.c` (priority queue operations), `sched.c` (scheduler implementation).
* **Memory Management:** `mm.c`, `mm-vm.c`, `mm-memphy.c` (Implementation of Paging-based memory management).
* *Legacy:* `paging.c`, `mem.c` (previous obsoleted versions for RAM and Virtual Memory).

### 🗂️ Build & Testing
* `Makefile`: Used to compile and build the OS simulation.
* `input/`: Contains a set of predefined inputs used to verify the system's functionality.
* `output/`: Contains sample outputs of the system for verification and comparison.

## 🚀 Getting Started
*(Bạn có thể bổ sung thêm hướng dẫn chạy code thực tế của bạn ở đây. Ví dụ bên dưới)*

**1. Build the project:**
```bash
make

```

**2. Run the simulation:**

```bash
./os [arguments]

```

**3. Verify with sample inputs:**
Check the `input/` folder for test cases and compare your results with the `output/` folder.

---

*This project is part of the Operating Systems course assignment, focusing on practical OS design and implementation via system calls.*
