# Check network connectivity
$Host = "google.com"
Test-Connection -ComputerName $Host -Count 4
