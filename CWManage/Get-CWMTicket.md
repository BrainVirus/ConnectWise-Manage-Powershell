# Get-CWMTicket
## SYNOPSIS
This function list tickets that match your condition.
## SYNTAX
```powershell
Get-CWMTicket [[-TicketID] <Int32>] [[-Condition] <String>] [[-orderBy] <Object>] [[-childconditions] <String>] [[-customfieldconditions] <String>] [[-page] <Int32>] [[-pageSize] <Int32>] [-all] [<CommonParameters>]
```
## PARAMETERS
### -TicketID &lt;Int32&gt;

```
Required                    false
Position                    1
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -Condition &lt;String&gt;
This is your search condition to return the results you desire.

Example:

(contact/name like "Fred%" and closedFlag = false) and dateEntered > [2015-12-23T05:53:27Z] or summary contains "test" AND  summary != "Some Summary"
```
Required                    false
Position                    2
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -orderBy &lt;Object&gt;
Choose which field to sort the results by
```
Required                    false
Position                    3
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -childconditions &lt;String&gt;
Allows searching arrays on endpoints that list childConditions under parameters
```
Required                    false
Position                    4
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -customfieldconditions &lt;String&gt;
Allows searching custom fields when customFieldConditions is listed in the parameters
```
Required                    false
Position                    5
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -page &lt;Int32&gt;
Used in pagination to cycle through results
```
Required                    false
Position                    6
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -pageSize &lt;Int32&gt;
Number of results returned per page (Defaults to 25)
```
Required                    false
Position                    7
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -all &lt;SwitchParameter&gt;
Return all results
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
PS C:\>Get-CWMTicket -TicketID 1

Returns ticket 1
```

### EXAMPLE 2
```powershell
PS C:\>Get-CWMTicket -all

Returns all tickets
```

### EXAMPLE 3
```powershell
PS C:\>Get-CWMTicket -condition 'summary="test"'

Returns the first 25 tickets with the summary of test
```

## NOTES
Author: Chris Taylor

Date: 10/10/2018 
## LINKS
http://labtechconsulting.com

https://developer.connectwise.com/products/manage/rest?a=Schedule&e=ScheduleEntries&o=GET

https://developer.connectwise.com/products/manage/rest?a=Service&e=Tickets&o=GETBYID
