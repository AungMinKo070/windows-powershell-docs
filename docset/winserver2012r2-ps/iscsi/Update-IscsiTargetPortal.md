---
external help file: iSCSITargetPortal.cdxml-help.xml
Module Name: iSCSI
ms.date: 10/29/2017
online version: https://docs.microsoft.com/powershell/module/iscsi/update-iscsitargetportal?view=windowsserver2012r2-ps&wt.mc_id=ps-gethelp
schema: 2.0.0
title: Update-IscsiTargetPortal
---
# Update-IscsiTargetPortal

## SYNOPSIS
Updates information about the specified iSCSI target portal.

## SYNTAX

### ByTargetPortalAddress (Default)

```
Update-IscsiTargetPortal [-TargetPortalAddress] <String[]> [-InitiatorInstanceName <String>]
 [-InitiatorPortalAddress <String>] [-TargetPortalPortNumber <UInt16>] [-CimSession <CimSession[]>]
 [-ThrottleLimit <Int32>] [-AsJob] [-PassThru] [<CommonParameters>]
```

### InputObject (cdxml)

```
Update-IscsiTargetPortal -InputObject <CimInstance[]> [-InitiatorInstanceName <String>]
 [-InitiatorPortalAddress <String>] [-TargetPortalPortNumber <UInt16>] [-CimSession <CimSession[]>]
 [-ThrottleLimit <Int32>] [-AsJob] [-PassThru] [<CommonParameters>]
```

## DESCRIPTION

The `Update-IscsiTargetPortal` cmdlet refreshes cached information about an iSCSI target portal.

## EXAMPLES

### Example 1: Update information about an iSCSI target portal

This command updates information about the specified iSCSI target portal.
The first command displays target portals by using the **Get-IscsiTargetPortal** cmdlet.

```powershell
Get-IscsiTargetPortal
```

```Output
InitiatorInstanceName      : 
InitiatorNodeAddress       : 
InitiatorPortalAddress     : 
InititorIPAdressListNumber : 4294967295 
IsDataDigest               : False 
IsHeaderDigest             : False 
TargetPortalAddress        : testiSCSI-deepcore 
TargetPortalPortNumber     : 3260
```

```powershell
C:\> Get-IscsiTargetPortal | Update-IscsiTargetPortal
```
The second command passes the same target portals to the current cmdlet to update them.

## PARAMETERS

### -AsJob

Runs the cmdlet as a background job. Use this parameter to run commands that take a long time to complete. 

The cmdlet immediately returns an object that represents the job and then displays the command prompt. 
You can continue to work in the session while the job completes. 
To manage the job, use the `*-Job` cmdlets. 
To get the job results, use the [Receive-Job](https://go.microsoft.com/fwlink/?LinkID=113372) cmdlet. 

For more information about Windows PowerShell background jobs, see [about_Jobs](https://go.microsoft.com/fwlink/?LinkID=113251).

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CimSession

Runs the cmdlet in a remote session or on a remote computer.
Enter a computer name or a session object, such as the output of a [New-CimSession](https://go.microsoft.com/fwlink/p/?LinkId=227967)
or [Get-CimSession](https://go.microsoft.com/fwlink/p/?LinkId=227966) cmdlet.
The default is the current session on the local computer.

```yaml
Type: CimSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InitiatorInstanceName

Specifies the name of the initiator instance that the iSCSI initiator service uses to send **SendTargets** requests to the target portal.
If no instance name is specified, the iSCSI initiator service chooses the initiator instance.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InitiatorPortalAddress

Specifies the IP address or DNS name that is associated with the portal.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet.

```yaml
Type: CimInstance[]
Parameter Sets: InputObject (cdxml)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru

Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetPortalAddress

Specifies the IP address or DNS name of the target portal.

```yaml
Type: String[]
Parameter Sets: ByTargetPortalAddress
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetPortalPortNumber

Specifies the TCP/IP port number for the target portal.
By default, the port number is `3260`.

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrottleLimit

Specifies the maximum number of concurrent operations that can be established to run the cmdlet.
If this parameter is omitted or a value of `0` is entered, then Windows PowerShellŪ calculates an
optimum throttle limit for the cmdlet based on the number of CIM cmdlets that are running on the computer.
The throttle limit applies only to the current cmdlet, not to the session or to the computer.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Management.Infrastructure.CimInstance#MSFT_IscsiTargetPortal

The `Microsoft.Management.Infrastructure.CimInstance` object is a wrapper class that displays Windows Management Instrumentation (WMI) objects.
The path after the pound sign (`#`) provides the namespace and class name for the underlying WMI object.

## OUTPUTS

### None

## NOTES

## RELATED LINKS

[iSCSI on TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee338476(v=ws.10))

[Storage on TechNet](https://go.microsoft.com/fwlink/?linkid=191356)

[Get-IscsiTargetPortal](./Get-IscsiTargetPortal.md)
