# Red Team Tools

## AMSI Bypass
Contains a powershell AMSI bypass method.

## AzureHound
Pure unmodified AzureHound EXE version 2.1.7. Collects information in Azure tenant.  
View results using BloodHound.  
Taken from https://github.com/BloodHoundAD/AzureHound/releases  

``azurehound.exe list -u "Username" -p "Password" -t "Domain name from https://portal.azure.com/#settings/directory page" -o "output.json"``

## BloodHound
File is too big for this page.  
Obtain EXE from [SpecterOps Page](https://github.com/SpecterOps/BloodHound/releases/tag/v5.7.1).  
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
- Cheatsheet here https://gist.github.com/insi2304/484a4e92941b437bad961fcacda82d49  

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

## PowerUp or PowerView in Local
In case you need to run PowerUp.ps1 or PowerView.ps1 on a local machine  
You need to bypass AV, execution policy and AMSI.  
1) Bypass AV by modifying the scripts till no detection, set an exception for C:\ in AV, or disable AV  
2) Bypass execution policy with powershell -ep bypass, or other methods [here](https://www.netspi.com/blog/technical/network-penetration-testing/15-ways-to-bypass-the-powershell-execution-policy/)  
3) Bypass or disable AMSI via method [here](https://rootrecipe.medium.com/advanced-powerup-ps1-usage-ad0f6d713a9f) or via other methods [here](https://gist.github.com/D3Ext/bf57673644ba08e729f65892e0dae6c4)  

- PowerUp Cheatsheet [here](https://viperone.gitbook.io/pentest-everything/resources/cheat-sheets/powerup)
- PowerView Cheatshee [here](https://book.hacktricks.xyz/windows-hardening/basic-powershell-for-pentesters/powerview)

## Rubeus
Rubeus EXE compiled, unzip and you'll immediately see Rubeus.exe.  
Taken from https://github.com/GhostPack/Rubeus

## Seatbelt
Seatbelt EXE compiled, look for it in "Seatbelt Compiled" folder.  
Taken from https://github.com/GhostPack/Seatbelt   

``Seatbelt.exe -group=all -full``

## SharPersist
Pure, unmodified SharPersist EXE version v1.0.1. Tried compiling source code but ran into plenty of issues.  
Taken from https://github.com/mandiant/SharPersist/releases/tag/v1.0.1   

``SharPersist.exe -t schtaskbackdoor -c "C:\Windows\System32\cmd.exe" -a "/c calc.exe" -n "NAME_OF_SCHEDULED_TASK" -m add``  
``SharPersist.exe -t startupfolder -c "C:\Windows\System32\cmd.exe" -a "/c calc.exe" -f "NAME_OF_LNK_FILE" -m add``

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

## Others Folder - Elevate System Trusted BOF
BOF tool used to escalate privilege.  
Taken from https://github.com/Mr-Un1k0d3r/Elevate-System-Trusted-BOF

## Others Folder - MiddleOut
EXE used to compress files.
https://github.com/RedSiege/MiddleOut

## Others Folder - Sharpkatz
Certain Mimikatz functionality converted into C#
Taken from https://github.com/b4rtik/SharpKatz

## Tips

### To compile SharPersist from source
1) Use Visual Studio 2022
2) Download SharPersist from https://github.com/mandiant/SharPersist and launch it in Visual Studio 2022
3) When prompted to "upgrade" to .NET Framework 4.8, go ahead with it
4) In Visual Studio, go to Tools > NuGet Package Manager > Package Manager Settings
5) Go to NuGet Package Manager > Package Sources, Add package source with URL https://api.nuget.org/v3/index.json
6) Go to Tools NuGet Package Manager > Manage NuGet Packages for Solution...
7) At top left, click Browse. Search for Costura.Fody, install version 3.3.3.
8) Then search for TaskScheduler, install version 2.8.11
9) Then compile the solution.
