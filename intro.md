# Introduction to PowerShell Scripting
## What is PowerShell?
PowerShell is a task automation framework from Microsoft, consisting of a command-line shell and the associated scripting language built on the .NET framework. 
Initially a Windows component only, PowerShell has been open-sourced and is now available across platforms (Windows, macOS, and Linux).

## Why Use PowerShell?
Automation: Automate repetitive tasks and manage system configurations.

Integration: Seamlessly integrate with other Microsoft products and services.

Extensibility: Easily extendable with custom cmdlets and scripts.

Cross-platform: Works on Windows, macOS, and Linux.

## PowerShell Basics
### Cmdlets
Cmdlets (pronounced "command-lets") are the basic building blocks of PowerShell. They are specialized .NET classes that perform a single function.

Syntax: Verb-Noun

Example: Get-Process, Set-Item, Remove-Item

### Common Cmdlets
Get-Help: Displays help about PowerShell cmdlets and concepts.
```powershell
Get-Help Get-Process
```

Get-Command: Gets all cmdlets, functions, workflows, aliases installed on your system.
```powershell
Get-Command
```

Get-Process: Gets the processes that are running on the local computer or a remote computer.
```powershell
Get-Process
```

Set-ExecutionPolicy: Changes the user preference for the PowerShell script execution policy.
```powershell
Set-ExecutionPolicy RemoteSigned
```

## PowerShell Scripts
A PowerShell script is a plain text file with a .ps1 extension that contains a series of commands. You can execute these scripts to perform complex operations.

### Creating and Running a Script

#### Creating a Script:
Open a text editor (e.g., Notepad, VS Code).
Write the PowerShell commands.
Save the file with a .ps1 extension.

#### Running a Script:
Open PowerShell.
Navigate to the script location.

#### Execute the script:
powershell
Copy code
.\script.ps1

### Basic Script Example

#### Create a file named HelloWorld.ps1 with the following content:

```powershell
# This is a comment
Write-Output "Hello, World!"
```

#### Run the script in PowerShell:

```powershell
.\HelloWorld.ps1
```
### Variables
Variables in PowerShell are used to store values. They are prefixed with a $ symbol.

```powershell
$greeting = "Hello, World!"
Write-Output $greeting
```
