# Clear event logs
Get-EventLog -LogName * | ForEach-Object { Clear-EventLog -LogName $_.Log }
