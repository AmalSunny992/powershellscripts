 # Create a new user
$Username = "newuser"
$Password = "P@ssw0rd" | ConvertTo-SecureString -AsPlainText -Force
New-LocalUser -Name $Username -Password $Password -FullName "New User" -Description "A new user account"
