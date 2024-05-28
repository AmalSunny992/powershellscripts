# Backup a directory
$Source = "C:\Users\username\Documents"
$Destination = "D:\Backup\Documents"
Copy-Item -Path $Source -Destination $Destination -Recurse
