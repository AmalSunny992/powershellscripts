# Managing Windows with PowerShell

## Objectives
- Learn how to manage files and directories using PowerShell
- Understand managing processes and services with PowerShell

## Concepts
### Managing Files and Directories

PowerShell provides cmdlets (commands) to manipulate files and directories similar to Unix-like systems.

**Commands:**
- New-Item: Creates a new item (file or directory).
    Example: New-Item -ItemType File -Path C:\path\to\file.txt

- Get-ChildItem: Lists files and directories in a specified location.
    Example: Get-ChildItem C:\path\to\directory

- Copy-Item: Copies files and directories.
    Example: Copy-Item -Path C:\source\file.txt -Destination C:\destination\file.txt

- Remove-Item: Deletes files and directories.
    Example: Remove-Item -Path C:\path\to\file.txt

### Managing Processes and Services
PowerShell allows management of processes (running programs) and services (background processes) on Windows.

**Commands:**
- Get-Process: Retrieves information about running processes.
    Example: Get-Process

- Stop-Process: Terminates one or more running processes.
    Example: Stop-Process -Name notepad

- Get-Service: Retrieves information about services.
    Example: Get-Service

- Start-Service: Starts a stopped service.
    Example: Start-Service -Name ServiceName

- Stop-Service: Stops a running service.
    Example: Stop-Service -Name ServiceName

## Summary
In this lesson, you explored managing Windows using PowerShell for file and directory operations, as well as managing processes and services. PowerShell provides powerful cmdlets for automation and administration tasks on Windows systems.
