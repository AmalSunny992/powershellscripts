 # Create a new user
$Username = "newuser"
$Password = "P@ssw0rd" | ConvertTo-SecureString -AsPlainText -Force
New-LocalUser -Name $Username -Password $Password -FullName "New User" -Description "A new user account"

# Add user to a group
$Username = "newuser"
$Group = "Administrators"
Add-LocalGroupMember -Group $Group -Member $Username

# Delete a user
$Username = "olduser"
Remove-LocalUser -Name $Username

# Backup a directory
$Source = "C:\Users\username\Documents"
$Destination = "D:\Backup\Documents"
Copy-Item -Path $Source -Destination $Destination -Recurse

# Check disk space
Get-PSDrive -PSProvider FileSystem | Select-Object Name, @{Name="Used(GB)";Expression={[math]::round($_.Used/1GB,2)}}, @{Name="Free(GB)";Expression={[math]::round($_.Free/1GB,2)}}, @{Name="Total(GB)";Expression={[math]::round($_.Used/1GB + $_.Free/1GB,2)}}

# Monitor CPU usage
Get-WmiObject win32_processor | Measure-Object -Property LoadPercentage -Average | Select-Object -Property Average

# Monitor CPU usage
Get-WmiObject win32_processor | Measure-Object -Property LoadPercentage -Average | Select-Object -Property Average

# List running processes
Get-Process | Select-Object -Property Name, CPU, ID, StartTime

# Restart a service
$ServiceName = "Spooler"
Restart-Service -Name $ServiceName

# Check network connectivity
$Host = "google.com"
Test-Connection -ComputerName $Host -Count 4

# Download a file
$Url = "https://example.com/file.zip"
$Destination = "C:\Downloads\file.zip"
Invoke-WebRequest -Uri $Url -OutFile $Destination

# Check Windows Update status
Get-WindowsUpdateLog


# Create a scheduled task to run a script daily
$Action = New-ScheduledTaskAction -Execute "powershell.exe" -Argument "C:\Scripts\DailyTask.ps1"
$Trigger = New-ScheduledTaskTrigger -Daily -At 6am
Register-ScheduledTask -Action $Action -Trigger $Trigger -TaskName "DailyTask" -Description "Runs a daily task"


# Clear event logs
Get-EventLog -LogName * | ForEach-Object { Clear-EventLog -LogName $_.Log }



# Get system information
Get-ComputerInfo | Select-Object -Property CsName, OsName, WindowsVersion, CsManufacturer, CsModel, CsTotalPhysicalMemory


# Compress a folder
$Folder = "C:\FolderToCompress"
$ZipFile = "C:\CompressedFolder.zip"
Add-Type -AssemblyName System.IO.Compression.FileSystem
[System.IO.Compression.ZipFile]::CreateFromDirectory($Folder, $ZipFile)
