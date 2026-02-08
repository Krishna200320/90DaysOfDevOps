Core Components of Linux
 Kernel

The core of the Linux operating system

Acts as a bridge between hardware and software

Responsible for:

Process management

Memory management

Device drivers

File system handling

Networking

👉 Without the kernel, applications cannot talk to hardware.

🔹 User Space

Area where user applications run

Includes:

Shell (bash, zsh)

System utilities (ls, cp, ps)

Applications (Docker, Nginx, etc.)

👉 User space communicates with kernel using system calls.

🔹 Init / systemd

First process started when Linux boots

Has Process ID (PID) = 1

Responsible for starting and managing system services

Most modern Linux systems use systemd instead of older init systems.

2. How Processes Are Created & Managed
Process Creation

Processes are created using:

fork() → Creates a copy of an existing process

exec() → Replaces process with a new program

Example:

When you run a command in terminal:

Shell creates a new process

Kernel assigns a PID

Process States
State	Meaning
Running	Process is actively using CPU
Sleeping	Waiting for input or resource
Stopped	Paused process
Zombie	Process finished but parent hasn't cleaned it
Orphan	Parent process terminated before child

👉 Zombie processes can waste system resources.

3. What systemd Does & Why It Matters
What systemd Does

Starts system services during boot

Manages background services (daemons)

Handles service restart policies

Manages logging via journal

Tracks service dependencies

Why systemd Matters in DevOps

Helps monitor services

Automatically restarts failed applications

Simplifies troubleshooting

