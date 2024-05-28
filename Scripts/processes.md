# List running processes
Get-Process | Select-Object -Property Name, CPU, ID, StartTime
