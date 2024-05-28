# Compress a folder
$Folder = "C:\FolderToCompress"
$ZipFile = "C:\CompressedFolder.zip"
Add-Type -AssemblyName System.IO.Compression.FileSystem
[System.IO.Compression.ZipFile]::CreateFromDirectory($Folder, $ZipFile)
