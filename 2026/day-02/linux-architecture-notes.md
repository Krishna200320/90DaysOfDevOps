# Linux Architecture Notes

## 1. Core Components of Linux

### Kernel
- The kernel is the **core of the Linux OS**.
- It manages:
  - CPU scheduling
  - Memory management
  - Hardware communication
  - Device drivers
  - Process management
- Acts as a bridge between hardware and software.

### User Space
- Where user applications run.
- Examples:
  - Shell (bash)
  - Text editors
  - Web servers
  - Package managers
- Users interact with Linux through user space tools which send requests to the kernel.


### Init / systemd
- First process started by Linux during boot.
- Process ID (PID) = 1
- Responsible for:
  - Starting system services
  - Managing background services (daemons)
  - Handling system startup and shutdown

Modern Linux distributions use **systemd** instead of older init systems.


## 2. How Processes Are Created and Managed

### Process Creation
- Every running program in Linux is a **process**.
- A new process is created using:
  - `fork()` → creates a copy of a process
  - `exec()` → replaces process with a new program

Each process has:
- PID (Process ID)
- Parent Process ID (PPID)
- Priority and resource allocation


### Process States

| State | Meaning |
|--------|------------|
| Running | Process is actively using CPU |
| Sleeping | Waiting for input or resource |
| Stopped | Process paused manually |
| Zombie | Process finished but parent hasn’t read exit status |

Zombie processes consume minimal resources but indicate poor process cleanup.

---

## 3. What systemd Does and Why It Matters

### What systemd Does
- Starts services during boot
- Restarts failed services automatically
- Manages service dependencies
- Provides logging through journal
- Controls system services using units

---

### Why systemd Matters for DevOps
- Helps monitor service health
- Makes troubleshooting easier
- Enables automatic service recovery
- Provides centralized logging

---
## Commands
ps aux
top
systemctl status
journalctl
kill

