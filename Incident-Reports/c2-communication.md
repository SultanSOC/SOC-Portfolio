# Incident Report: Suspicious C2 Communication via HTTP

## 1. Summary
An alert triggered by the IDS indicated potential command-and-control (C2) communication from a host in the HR department. 
Further investigation of HTTP connection logs confirmed that the host accessed suspicious external content consistent with C2 activity.

---

## 2. Alert Details
- Alert Source: IDS
- Severity: High
- Date: March 2022

---

## 3. Affected Asset(s)
- IP Address: 192.166.65.54
- Department: HR

---

## 4. Evidence
- External Domain: pastebin.com
- Full URL: pastebin.com/yTg0Ah6a
- File Accessed: secret.txt
- Activity Type: HTTP outbound request to file-sharing service

---

## 5. Analysis
The host established outbound communication with a public file-sharing platform known to be abused by attackers for command-and-control purposes.
The retrieved file suggests possible staging or data exchange between the compromised host and an external attacker. 
The use of legitimate web services allows attackers to blend malicious traffic with normal user behavior, making detection more difficult.

---

## 6. Conclusion
- Classification: True Positive
- Attack Type: Command and Control (C2 Communication)

---

## 7. Recommendations
- Isolate the affected host for further investigation
- Block access to the identified domain and URL
- Monitor for similar outbound connections to file-sharing platforms
- Apply web filtering and threat intelligence feeds
