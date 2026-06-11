# SAP System Down Analysis

## Objective

Identify and resolve SAP system downtime issues.

## Steps

### 1. Check SAP Services

Transaction:
- SM51
- SM66

OS Level:

```bash
sapcontrol -nr <Instance_Number> -function GetProcessList
