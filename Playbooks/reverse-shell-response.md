# Playbook: Reverse Shell Response

## 1. Validate the Alert
- Review the alert details
- Identify the affected host
- Check the destination IP and port

---

## 2. Investigate
- Identify the process creating the connection
- Check parent and child processes
- Determine if the destination IP is external
- Review recent command-line activity

---

## 3. Contain
If malicious:
- Isolate the affected endpoint
- Block the malicious IP if appropriate
- Prevent further communication

---

## 4. Escalate
Escalate if:
- Reverse shell activity is confirmed
- Privileged accounts are involved
- Multiple hosts show similar behavior
- Persistence or lateral movement is detected

---

## 5. Recover
- Remove malicious artifacts
- Verify the host is clean
- Continue monitoring for suspicious outbound connections
