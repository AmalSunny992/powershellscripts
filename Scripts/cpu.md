# Monitor CPU usage
Get-WmiObject win32_processor | Measure-Object -Property LoadPercentage -Average | Select-Object -Property Average
