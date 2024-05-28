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
### Control Structures
#### If-Else
```powershell
$number = 10
if ($number -gt 5) {
    Write-Output "The number is greater than 5"
} else {
    Write-Output "The number is 5 or less"
}
```
#### Loops
##### For Loop
```powershell
for ($i = 0; $i -lt 5; $i++) {
    Write-Output "Iteration $i"
}
```
##### Foreach Loop
```powershell
$array = 1, 2, 3, 4, 5

foreach ($item in $array) {
    Write-Output "Item: $item"
}
```
##### While Loop
```powershell
$i = 0

while ($i -lt 5) {
    Write-Output "Iteration $i"
    $i++
}
```
#### Functions
Functions allow you to group commands into a reusable block.

```powershell
function Get-Greeting {
    param (
        [string]$Name
    )
    return "Hello, $Name!"
}

# Call the function
$greeting = Get-Greeting -Name "Alice"
Write-Output $greeting
```

#### Error Handling
PowerShell provides error handling mechanisms to manage script errors gracefully.

```powershell
try {
    # Code that might throw an exception
    $content = Get-Content -Path "nonexistentfile.txt"
} catch {
    # Handle the error
    Write-Output "An error occurred: $_"
}
```
