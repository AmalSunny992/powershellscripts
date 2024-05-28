# Create a scheduled task to run a script daily
$Action = New-ScheduledTaskAction -Execute "powershell.exe" -Argument "C:\Scripts\DailyTask.ps1"
$Trigger = New-ScheduledTaskTrigger -Daily -At 6am
Register-ScheduledTask -Action $Action -Trigger $Trigger -TaskName "DailyTask" -Description "Runs a daily task"
