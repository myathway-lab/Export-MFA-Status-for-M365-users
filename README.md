# Export-MFA-Status-for-M365-users

## We need Global admin to export the MFA status. 


 
## As per the script, it will retrive all the users except Guest users.


$Users = Get-MsolUser -All | Where-Object { $_.UserType -ne "Guest" }
 

## To export the user name "mya@example.com", we can edit the script like this. 

$Users = Get-MsolUser -All | Where-Object { $_.UserType -eq "mya@example.com" }
