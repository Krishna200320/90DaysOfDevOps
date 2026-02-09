# Linux Commands Cheat Sheet

## Process Management

### ps aux
Shows all running processes.

### top
Displays real-time CPU and memory usage.

### htop
Interactive process viewer (improved version of top).

### kill <PID>
Stops a process using its process ID.

### pkill <name>
Kills processes by name.

### systemctl status <service>
Checks service status.

### systemctl restart <service>
Restarts a service.

---

## File System Commands

### ls
Lists files and directories.

### cd <directory>
Changes directory.

### pwd
Shows current directory path.

### mkdir <name>
Creates a new directory.

### rm <file>
Deletes a file.

### rm -r <directory>
Deletes a directory and its contents.

### cp <source> <destination>
Copies files or directories.

### mv <source> <destination>
Moves or renames files.

### cat <file>
Displays file content.

### nano <file>
Opens file in text editor.

---

## Disk & Memory Monitoring

### df -h
Shows disk space usage.

### du -sh <folder>
Shows folder size.

### free -h
Displays memory usage.

---

## Networking Troubleshooting

### ping <host>
Checks network connectivity.

### ip addr
Shows IP address and network interfaces.

### curl <URL>
Tests web connectivity and fetches data.

### dig <domain>
Checks DNS resolution.

### ss -tuln
Shows open ports and listening services.

---

## Log Monitoring

### tail -f <file>
Shows live log updates.

### journalctl
Displays system logs.

---

## Summary
These commands help monitor processes, manage files, troubleshoot networks, and inspect system health. They are essential for daily Linux and DevOps operations.
