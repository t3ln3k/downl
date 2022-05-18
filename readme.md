https://raw.githubusercontent.com/olafhartong/sysmon-modular/master/sysmonconfig.xml

https://docs.microsoft.com/en-us/sysinternals/downloads/procmon

https://docs.microsoft.com/en-us/sysinternals/downloads/process-explorer

https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon

https://www.elastic.co/es/downloads/beats/winlogbeat

https://www.elastic.co/guide/en/beats/winlogbeat/master/winlogbeat-reference-yml.html

### Install Atomic Red Team
```powershell
Install-Module -Name invoke-atomicredteam.powershell-yaml -Scope CurrentUser
```
 #### If error:
 ```powershell
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
Install-PackageProvider -Name NuGet
```
```powershell
IEX (IWR 'https://raw.githubusercontent.com/redcanaryco/invoke-atomicredteam/master/install-atomicredteam.ps1' -UseBasicParsing);
Install-AtomicRedTeam -getAtomics

Import-Module "C:\AtomicRedTeam\invoke-atomicredteam\Invoke-AtomicRedTeam.psd1" -Force
$PSDefaultParameterValues = @{"Invoke-AtomicTest:PathToAtomicsFolder"="C:\AtomicRedTeam\atomics"}
```
