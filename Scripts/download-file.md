# Download a file
$Url = "https://example.com/file.zip"
$Destination = "C:\Downloads\file.zip"
Invoke-WebRequest -Uri $Url -OutFile $Destination
