# New-CWMProjectTeamMember
## SYNOPSIS
This function will create a new ticket.
## SYNTAX
```powershell
New-CWMProjectTeamMember [-ProjectID] <Int32> [[-id] <Int32>] [[-hours] <Decimal>] [-member] <Object> [-projectRole] <Object> [[-workRole] <Object>] [[-startDate] <String>] [[-endDate] <String>] [[-_info] <Object>] [<CommonParameters>]
```
## PARAMETERS
### -ProjectID &lt;Int32&gt;

```
Required                    true
Position                    1
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -id &lt;Int32&gt;

```
Required                    false
Position                    2
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -hours &lt;Decimal&gt;

```
Required                    false
Position                    3
Default value                0
Accept pipeline input       false
Accept wildcard characters  false
```
### -member &lt;Object&gt;

```
Required                    true
Position                    4
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -projectRole &lt;Object&gt;

```
Required                    true
Position                    5
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -workRole &lt;Object&gt;

```
Required                    false
Position                    6
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -startDate &lt;String&gt;

```
Required                    false
Position                    7
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -endDate &lt;String&gt;

```
Required                    false
Position                    8
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -_info &lt;Object&gt;

```
Required                    false
Position                    9
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
## EXAMPLES
### EXAMPLE 1
```powershell
PS C:\>$Ticket = @{

'identifier' = $Product.offerName
    'description' = $Product.offerName
    'subcategory' = @{id = 152}
    'type' = @{id = 47}
    'customerDescription' = $Product.offerName
    'cost' = $Product.unitPrice
    'price' = $Price
    'manufacturerPartNumber' = $Product.offerName
    'manufacturer' = $Manufacturer
    'productClass' = 'Agreement'
    'taxableFlag' = $true
}
New-CWTicket @Ticket
```

## NOTES
Author: Chris Taylor

Date: 8/22/2018 
## LINKS
http://labtechconsulting.com

https://developer.connectwise.com/products/manage/rest?a=Project&e=ProjectsTeamMembers&o=CREATE
