# Export-MFA-Status-for-M365-users

<br>

### We must have Global admin to export the MFA status. 

<br>
 
### As per the script, it will retrive all the users except Guest users.

<br>

$Users = Get-MsolUser -All | Where-Object { $_.UserType -ne "Guest" }
 
<br>

### To export the user name "mya@example.com", we can edit the script like this. 

<br>

$Users = Get-MsolUser -All | Where-Object { $_.UserType -eq "mya@example.com" }
