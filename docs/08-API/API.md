---
title: API
---
## Overview
This section is an overview of the application programming interface (API) for the team project in correspondence to the metal detection subsystem. Listed blow are the message that shall take place between subsytems.


## This Subsystem's ID
* Metal Detection: m

### All Subsystem IDs

| Subsystem | ID |
|-----------|-----|
| HMI | 'h' |
| Comm | 'c' |
| Wheel | 'w' |
| Pressure | 'P' |
| Arm | 'a' |
| Metal | 'm' |
| Temp | 't' |


## Recieved Messages
### Message: Read Output
For telling the metal detection system to read the output value and prepare to return message with the corresponding data.


| Field | Bytes | Section Name | Type | Min Recognized | Max Recognized | Example |
|-------|-------|---------------|------------------------|----------------|----------------|---------|
| Variable | 2 | MR | string | -- | -- | MR |
| Separator | 1 | : | char | : | : | : |
| Type Identifier | 1 | S | string | -- | -- | S |
| Separator | 1 | : | char | : | : | : |
| Value | 4 | read | string | -- | -- | read |
| Terminator | 1 | ; | char | ; | ; | ; |

**Total Message Data Bytes: 10**

### Valid Example Packet:
**AZhmMR:S:read:YB**

## Meaning:
- AZ = Start
- h = HMI subsystem
- m = Metal detection subsystem
- S = type string
- read = command
- YB = End


## Messages Sent
### Message: MD Output
For telling the HMI subsystem the output value of the metal detection system.


| Field | Bytes | Section Name | Type | Min Recognized | Max Recognized | Example |
|-------|-------|---------------|------------------------|----------------|----------------|---------|
| Variable | 2 | MD | string | -- | -- | MD |
| Separator | 1 | : | char | : | : | : |
| Type Identifier | 1 | S | string | -- | -- | S |
| Separator | 1 | : | char | : | : | : |
| Value | 1 | T/F | string | F | T | T |
| Terminator | 1 | ; | char | ; | ; | ; |

**Total Message Data Bytes: 7**

### Valid Example Packet:
**AZmhMD:S:T:YB**

## Meaning:
- AZ = Start
- m = Metal detection subsystem
- h = HMI subsystem
- S = type string
- T = output(True)
- YB = End


## Messages Broadcast
### Message: LED(ON)
This broadcast message tells every subsystem connected to turn on their LED to indicate connection ready. Mainly sourced from the HMI subsystem.


| Field | Bytes | Section Name | Type | Min Recognized | Max Recognized | Example |
|-------|-------|---------------|------------------------|----------------|----------------|---------|
| Variable | 2 | ST | string | -- | -- | ST |
| Separator | 1 | : | char | : | : | : |
| Type Identifier | 1 | S | string | -- | -- | S |
| Separator | 1 | : | char | : | : | : |
| Value | 5 | Start | string | -- | -- | Start |
| Terminator | 1 | ; | char | ; | ; | ; |

**Total Message Data Bytes: 11**

### Valid Example Packet:
**AZhXST:S:Start:YB**

## Meaning:
- AZ = Start
- h = HMI subsystem
- X = Everyone
- S = type string
- Start = Subsystem LED(ON)
- YB = End

## Behavior rules (ID: m)
### Recieving
- Check message validity
    - If invalid, then output error, then trash
    - If valid, then continue

- Check source
    - If source = 'm', then output error, then trash
    - Otherwise continue

- Check destination
    - If destination is not 'm', then pass
    - If destination is 'm', then continue
    - If destination is 'X', then continue  

- Identify Varible Name

- Identify Varible Type

- Identify Varible Value

- Handle message in system
    - If destination stated 'm', then trash, then create new message to source
    - If destination stated 'X', then pass

### Sending
- Send MD (Metal detected) data to source h (HMI subsystem)
    - If value = True, send AZmhMD:S:T:YB
    - If vaule - False, send AZmhMD:S:F:YB


