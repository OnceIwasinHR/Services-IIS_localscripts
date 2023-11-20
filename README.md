# Services-IIS_localscripts
Includes all local scripts and readme files for how to use them. Used them for work on a daily basis.

# 1. Item is Powershell script
This powershell script will locate if any associated application service is 'not running' or Stopped. Based on the string name and setup, it is to call and start the [service] on demand. 
(**Important Note:** This powershell script was created to be associated with scaduled task via Windows BUILT IN Task Schadular. Based on organizational needs, the schaduled task frequency can be set up. SYSTEM account or local machine administrator account has to be associated for this Schaduled Task to work and call automatically, and has to be set up to run even when account is NOT LOGGED IN.)

--Detail and background information.
-The Problem: .exe Application for client has windows service associated and running on host application server, on premise. Data base server is seperate and does not contain or need this service. During server reboot, the service stops and whe server is online, the service should restart itself. However, occasionally it is not starting on it's own and the data transfer using the service, from Database A to Databse B (WHILE both database are in same databse server, this services job is to transfer data from 1 to the another on a frequent basis.

-The solution: 1 powershell script containing both all services informaiton for LIVE Application Host server and associate it with Schaduled task to call on a frequent basis if status = 'not running' 
