# Detection Note: Reverse Shell Detection

## 1. Overview
A reverse shell occurs when a compromised system initiates a connection to an external attacker, allowing remote control.

---

## 2. Why It Matters
It gives attackers full control over the system.

---

## 3. Key Indicators
- Outbound connection to external IP
- Uncommon port (e.g., 4444, 1337)
- Suspicious process (cmd.exe, powershell.exe)
- Continuous connection

---

## 4. Detection Logic
Look for internal hosts making outbound connections to external IPs over uncommon ports, especially when associated with command-line processes.

---

## 5. Example Scenario
Internal host connects to external IP on port 4444 using powershell.

---

## 6. False Positives
- Developers or testing environments

---

## 7. Conclusion
Unusual outbound connections with command execution may indicate reverse shell activity.
