# Common SAP BASIS Interview Scenarios

## Scenario 1: SAP System Is Slow

### Question

A user reports that the SAP system is very slow. How would you troubleshoot?

### Approach

Step 1:
Check Work Processes

Transaction:

```
SM50
SM66
```

Step 2:
Analyze Workload

Transaction:

```
ST03N
```

Step 3:
Check Operating System Performance

Transaction:

```
ST06
```

Step 4:
Review Database Performance

Transaction:

```
DBACOCKPIT
```

Step 5:
Analyze System Logs

Transaction:

```
SM21
```

### Expected Outcome

Identify whether the issue is related to SAP, OS, Database, or Network.

---

## Scenario 2: User Unable to Login

### Question

A user cannot log in to SAP. What checks would you perform?

### Approach

1. Verify User Status

Transaction:

```
SU01
```

2. Check if User is Locked

3. Verify Password Status

4. Check License Availability

5. Review Security Logs

Transaction:

```
SM20
```

### Resolution

Unlock User and reset password if required.

---

## Scenario 3: Background Job Cancelled

### Question

A critical background job has failed. What would you do?

### Approach

1. Check Job Status

Transaction:

```
SM37
```

2. Review Job Log

3. Analyze Short Dumps

Transaction:

```
ST22
```

4. Review System Logs

Transaction:

```
SM21
```

### Resolution

Correct the root cause and re-execute the job.

---

## Scenario 4: RFC Connection Failure

### Question

RFC destination is failing. How would you troubleshoot?

### Approach

Transaction:

```
SM59
```

Checks:

- Connection Test
- Authorization Test
- Hostname Verification
- User Credentials
- Network Connectivity

### Resolution

Correct RFC configuration and validate connectivity.

---

## Scenario 5: Transport Request Not Imported

### Question

A transport request failed during import. What is your approach?

### Approach

Transaction:

```
STMS
```

Check:

- Import Logs
- Return Code
- Transport Route
- Dependent Requests

### Resolution

Fix the identified issue and re-import the transport.

---

## Scenario 6: Update Requests Failed

### Question

Business users report that data is not updating. How would you investigate?

### Approach

Transaction:

```
SM13
```

Check:

- Failed Updates
- Error Details
- System Logs
- Database Status

### Resolution

Resolve the root cause and repeat the update request.

---

## Scenario 7: Work Processes Fully Utilized

### Question

All dialog work processes are occupied. What will you do?

### Approach

Transactions:

```
SM50
SM66
```

Check:

- Long Running Processes
- Locked Processes
- CPU Utilization
- Background Job Activity

### Resolution

Optimize workload and terminate stuck processes if necessary.

---

## Scenario 8: Database Space Issue

### Question

Database space is running low. How would you handle it?

### Approach

Transaction:

```
DBACOCKPIT
```

Check:

- Tablespace Usage
- Data Growth
- Archive Opportunities

### Resolution

Extend storage or perform housekeeping activities.

---

## Key Transactions for SAP BASIS Interviews

| Area | Transaction |
|--------|------------|
| Work Process Monitoring | SM50 |
| Global Process Monitoring | SM66 |
| System Logs | SM21 |
| Short Dumps | ST22 |
| Background Jobs | SM37 |
| Update Requests | SM13 |
| RFC Monitoring | SM59 |
| User Administration | SU01 |
| Workload Analysis | ST03N |
| OS Monitoring | ST06 |
| Database Administration | DBACOCKPIT |
| Transport Management | STMS |

## Conclusion

These scenarios represent common SAP BASIS administration activities and are frequently discussed during technical interviews. A structured troubleshooting approach helps identify issues quickly and ensures system stability.
