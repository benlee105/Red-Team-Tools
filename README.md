# Red Team Tools

## AzureHound
Pure unmodified AzureHound EXE version 2.1.7. Collects information in Azure tenant.  
View results using BloodHound.  
Taken from https://github.com/BloodHoundAD/AzureHound/releases

``AzureHound.exe list -u "Username" -p "Password" -t "Domain name from https://portal.azure.com/#settings/directory page" -o "output.json"``

## BloodHound
Pure unmodified BloodHound EXE version 4.3.1. Displays information from AzureHound and SharpHound.  
If you don't want to install EXE, see "BloodHound Docker" section below.
Taken from https://github.com/BloodHoundAD/BloodHound/releases/tag/v4.3.1

## BloodHound Docker
Docker image from SpectreOps. Obtain using curl + docker commands.  
Password is randomly generated in the terminal output.  
After curl command below, access http://localhost:8080/ui/login, username admin, password from terminal output.  
``curl -L https://raw.githubusercontent.com/SpecterOps/bloodhound/main/examples/docker-compose/docker-compose.yml | docker compose -f - up``  

## Kerbeus (Rubeus in BOF Form)
Rubeus in BOF format.  
Taken from https://github.com/RalfHacker/Kerbeus-BOF

## Outflank C2 BOFs
Contains some BOFs that could be useful.  
Taken from https://github.com/outflanknl/C2-Tool-Collection?tab=readme-ov-file

## PrivKit BOF
Cobalt Strike BOF for priv esc checking.  
Taken from https://github.com/mertdas/PrivKit

``beacon> privcheck``

## TrustedSec Remote OPs BOF
TrustedSec's BOFs for post-exploitation.  
Taken from https://github.com/trustedsec/CS-Remote-OPs-BOF

## TrustedSec Situation Awareness BOF
TrustedSec's BOFs for scanning.  
Taken from https://github.com/trustedsec/CS-Situational-Awareness-BOF

## Certify
Certify EXE compiled, unzip and you'll immediately see Certify.exe  
**If you're looking for Certipy, use python command "pip3 install certipy-ad" instead**  
Taken from https://github.com/GhostPack/Certify
Taken from https://github.com/ly4k/Certipy

## Mimikatz
Pure, unmodified mimikatz version 2.2.0-20220919. Tried compiling source code but ran into plenty of issues.  
Taken from https://github.com/gentilkiwi/mimikatz/releases

## Nmap
EXE installer for nmap on Windows. Self explanatory!  
Taken from https://nmap.org/download.html

## Winpeas in PEASS-NG
Couldn't compile EXE, .NET version might be too old. Use BAT or PS1 instead.  

## PowerSploit
Invoke-Mimikatz is in Exfiltration folder.  
PowerUp is in Privesc folder.  
PowerView is in Recon folder.  
  
``To load script into Cobalt Strike, use powershell-import xx.ps1``  
``To load script into powershell, use . .\xx.ps1``

## Rubeus
Rubeus EXE compiled, unzip and you'll immediately see Rubeus.exe.  
Taken from https://github.com/GhostPack/Rubeus

## Seatbelt
Seatbelt EXE compiled, look for it in "Seatbelt Compiled" folder.  
Taken from https://github.com/GhostPack/Seatbelt   

``Seatbelt.exe -group=all``

## SharPersist
Pure, unmodified SharPersist EXE version v1.0.1. Tried compiling source code but ran into plenty of issues.  
Taken from https://github.com/mandiant/SharPersist/releases/tag/v1.0.1   

``SharPersist.exe -t schtaskbackdoor -c "C:\Windows\System32\cmd.exe" -a "/c calc.exe" -n "NAME_OF_SCHEDULED_TASK" -m add``  
``SharPersist.exe -t startupfolder -c "C:\Windows\System32\cmd.exe" -a "/c calc.exe" -f "Some File" -m add``

## SharpHound
Pure, unmodified SharpHound EXE version v2.3.2.  
View results using BloodHound.  
Taken from https://github.com/BloodHoundAD/SharpHound/releases  

``SharpHound.exe -c all``

## SharpUp
PowerUp.ps1 in C# format. EXE compiled, unzip and you'll immediately see SharpUp.exe.  
Taken from https://github.com/GhostPack/SharpUp  

``SharpUp.exe audit``

## Snaffler
Used to identify credentials in an AD environment.  
Snaffler EXE compiled, unzip and you'll immediately see Snaffler.  
Taken from https://github.com/SnaffCon/Snaffler  

``snaffler.exe -s -o snaffler.log``

## More BOFs
Refer to URL for more useful BOFs - https://github.com/wsummerhill/C2_RedTeam_CheatSheets/blob/main/CobaltStrike/BOF_Collections.md
