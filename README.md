# Export-MFA-Status-for-M365-users

<br>

### We must have Global admin to export the MFA status. 

<br>
 
### As per the script, it will retrive all the users except Guest users.

<br>

$Users = Get-MsolUser -All | Where-Object { $_.UserType -ne "Guest" }
 
<br>

### To export the specific user "mya@example.com", we can edit the script like this. 

<br>

$Users = Get-MsolUser -All | Where-Object { $_.UserType -eq "mya@example.com" }


### To export the sepcific multiple  users, we can combine all the user in csv like this. 

<br>

$Users = Import-CSV C:\path\file.csv

