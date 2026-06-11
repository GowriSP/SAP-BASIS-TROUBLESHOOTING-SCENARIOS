This document explains the steps followed by SAP BASIS administrators when an SAP system becomes unavailable.

## Symptoms

- Users unable to log in
- SAP GUI connection failure
- Transactions not responding
- Dispatcher stopped

## Troubleshooting Steps

### Step 1: Verify SAP Instance Status

Command:

```bash
sapcontrol -nr <Instance_Number> -function GetProcessList
```

Expected Result:
All SAP processes should display GREEN status.

### Step 2: Check Work Processes

Transaction Code:

```
SM50
```

Verify:

- Running Work Processes
- Stopped Processes
- Long Running Processes

### Step 3: Review System Logs

Transaction Code:

```
SM21
```

Check for:

- Dispatcher Errors
- Database Errors
- Memory Issues
- Operating System Messages

### Step 4: Analyze Short Dumps

Transaction Code:

```
ST22
```

Review runtime errors and identify the root cause.

### Step 5: Verify Database Availability

Database should be online and accessible.

Example:

- SAP HANA Database Running
- Tenant Database Available

## Resolution

- Restart SAP Services if required
- Resolve Database Connectivity Issues
- Clear Resource Bottlenecks
- Verify System Health After Recovery

## Conclusion

A structured troubleshooting approach helps BASIS administrators quickly identify and resolve SAP system outages.
