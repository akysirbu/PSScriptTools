---
external help file: PSScriptTools-help.xml
Module Name: PSScriptTools
online version: 
schema: 2.0.0
---

# Get-PSWho

## SYNOPSIS
Get PowerShell user summary information

## SYNTAX

```
Get-PSWho [-AsString]
```

## DESCRIPTION
This command will provide a summary of relevant information for the current  user in a PowerShell session. You might use this to troubleshoot an end-user problem running a script or command.

The default behavior is to write an object to the pipeline, but you can use the -AsString parameter to force the command to write a string. This makes it easier to use in your scripts with Write-Verbose.

## EXAMPLES

### Example 1
```
PS C:\> Get-PSWho

User            : BOVINE320\Jeff
Elevated        : True
Computername    : BOVINE320
OperatingSystem : Microsoft Windows 10 Pro \[64-bit\]
OSVersion       : 10.0.16299
PSVersion       : 5.1.16299.64
Edition         : Desktop
PSHost          : ConsoleHost
WSMan           : 3.0
ExecutionPolicy : RemoteSigned
Culture         : en-US
```
### Example 2
```
PS /home/jhicks> Get-PSWho

User            : jhicks
Elevated        : NA
Computername    : Bovine320
OperatingSystem : Linux 4.4.0-43-Microsoft #1-Microsoft Wed Dec 31 14:42:53 PST 2014
OSVersion       : Ubuntu 16.04.3 LTS
PSVersion       : 6.0.0-rc
Edition         : Core
PSHost          : ConsoleHost
WSMan           : 3.0
ExecutionPolicy : Unrestricted
Culture         : en-US
```

### Example 3
```
PS C:\> Get-PSWho

User            : BOVINE320\Jeff
Elevated        : True
Computername    : BOVINE320
OperatingSystem : Microsoft Windows 10 Pro \[64-bit\]
OSVersion       : 10.0.16299
PSVersion       : 6.0.0-rc
Edition         : Core
PSHost          : ConsoleHost
WSMan           : 3.0
ExecutionPolicy : RemoteSigned
Culture         : en-US
```

### Example 4
```
PS C:\> Get-PSWho -asString | Set-Content c:\test\who.txt
```

## PARAMETERS

### -AsString
Write the summary object as a string.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### none

## OUTPUTS

### [pscustomobject]
### [system.string]

## NOTES
Learn more about PowerShell: http://jdhitsolutions.com/blog/essential-powershell-resources/

## RELATED LINKS

[Get-CimInstance]()

[Get-ExecutionPolicy]()

[$PSVersionTable]()

[$Host]()
