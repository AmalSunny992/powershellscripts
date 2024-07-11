# Using PowerShell for Automation

## Objectives
- Learn how to automate tasks with PowerShell scripts
- Understand how to schedule tasks in Windows

## Concepts
### Automating Tasks with PowerShell Scripts

PowerShell scripts can automate repetitive tasks, streamline system management, and perform complex operations.

Writing a PowerShell Script:
- Open a text editor (e.g., Notepad).
- Write your PowerShell commands.
- Save the file with a .ps1 extension.


Example Script: automate_task.ps1
```powershell
# PowerShell script to clean up temporary files
$TempPath = "C:\Temp"
Get-ChildItem -Path $TempPath -Recurse -Force | Remove-Item -Force -Recurse
Write-Output "Temporary files cleaned up from $TempPath"
```

Running a PowerShell Script:

``` powershell
# Execute the script
.\automate_task.ps1
```

### Scheduled Tasks in Windows
Windows Task Scheduler allows you to schedule PowerShell scripts to run at specified times or intervals.

**Creating a Scheduled Task:**
- Open Task Scheduler (taskschd.msc).
- Create a new task:
    - General: Provide a name and description.
    - Triggers: Define when the task should run (e.g., daily, weekly).
    - Actions: Specify the action to perform (e.g., start a program).
        - Program/script: powershell.exe
        - Add arguments: -File "C:\path\to\your\script.ps1"

**Example:**
To schedule the automate_task.ps1 script to run daily at 3 AM:

- Open Task Scheduler.
- Click "Create Basic Task".
- Follow the wizard to set the schedule and specify the script to run.

## Summary
In this lesson, you learned how to use PowerShell for automation, including writing scripts and scheduling tasks using Windows Task Scheduler. Automation is a key aspect of efficient system administration and maintenance.