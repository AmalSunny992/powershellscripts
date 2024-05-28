# Add user to a group
$Username = "newuser"
$Group = "Administrators"
Add-LocalGroupMember -Group $Group -Member $Username
