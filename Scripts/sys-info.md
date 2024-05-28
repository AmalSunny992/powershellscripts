# Get system information
Get-ComputerInfo | Select-Object -Property CsName, OsName, WindowsVersion, CsManufacturer, CsModel, CsTotalPhysicalMemory
