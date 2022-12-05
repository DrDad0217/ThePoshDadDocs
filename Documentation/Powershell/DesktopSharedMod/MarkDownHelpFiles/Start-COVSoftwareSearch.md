# Start-COVSoftwareSearch

#Documentation

## SYNOPSIS
Start-COVSoftwareSearch is used to query all installed software on a remote computer 

## SYNTAX

```
Start-COVSoftwareSearch [-ComputerName] <String[]> [<CommonParameters>]
```

## DESCRIPTION
This function can be used to run software queries across multiple remote computers, it accepts pipeline input ByValue and ByPropertyName

## EXAMPLES

### Example 1
```powershell
PS C:\> Start-COVSoftwareSearch -Computername INT012055T
```

This example will fetch all installed software on the remote machine

## PARAMETERS

### -ComputerName
{{ Fill ComputerName Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String[]

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

