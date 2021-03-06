# ConvertTo-CWMTime
## SYNOPSIS
Converts [datetime] to the time format used in condition queries.
## SYNTAX
```powershell
ConvertTo-CWMTime [[-Date] <DateTime>] [-Raw] [<CommonParameters>]
```
## DESCRIPTION
This will convert an input to a universal date time object then output in a format used by the ConnectWise Manage API.
## PARAMETERS
### -Date &lt;DateTime&gt;
Date used in conversion.
```
Required                    false
Position                    1
Default value
Accept pipeline input       true (ByValue)
Accept wildcard characters  false
```
### -Raw &lt;SwitchParameter&gt;

```
Required                    false
Position                    named
Default value                False
Accept pipeline input       false
Accept wildcard characters  false
```
## EXAMPLES
### EXAMPLE 1
```powershell
PS C:\>ConvertTo-CWMTime $(Get-Date).AddDays(1)

Will output tomorrows date.
```

## NOTES
Author: Chris Taylor

Date: 10/16/2018 
