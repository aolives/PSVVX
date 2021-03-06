﻿---
external help file: PSVVX-help.xml
Module Name: PSVVX
online version: https://github.com/zloeber/PSVVX
schema: 2.0.0
---

# Find-VVXDevice

## SYNOPSIS
Discovers a VVX device.

## SYNTAX

```
Find-VVXDevice [-Device] <String> [-Port <Int32>] [-DiscoveryWaitTime <Int32>] [-LocalIP <String>]
 [-LocalPort <Int32>]
```

## DESCRIPTION
Discovers a VVX device.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Find-VVXDevice -Device '192.168.1.100'
```

Checks to see if the device at 192.168.1.100 is a VVX device.

## PARAMETERS

### -Device
Device to discover.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Phone, DeviceName, IP

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Port
Port to use for remote device connection.
Default is 5060.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 5060
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiscoveryWaitTime
Time in ms to wait for responses.
Defaults to 350ms

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 350
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalIP
Local IP address to use for connection to device.
Defaults to an autodiscovered IP of the local system.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: (Get-PIIPAddress | Select -First 1).IP.ToString()
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalPort
Local port to use for connection to device.
Defaults to a random unused high port.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: (Get-UnusedHighPort)
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES
Author: Zachary Loeber

## RELATED LINKS

[https://github.com/zloeber/PSVVX](https://github.com/zloeber/PSVVX)

