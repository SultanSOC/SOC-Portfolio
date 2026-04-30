# Detection Note: Command and Control (C2) Communication

## 1. Overview
Compromised systems communicate with attacker-controlled servers.

---

## 2. Why It Matters
Allows attackers to control infected systems.

---

## 3. Key Indicators
- Outbound traffic to suspicious domains
- Use of public services (pastebin, file-sharing)
- Repeated communication patterns

---

## 4. Detection Logic
Analyze outbound traffic for connections to suspicious or unusual domains.

---

## 5. Example Scenario
Host connects to pastebin to retrieve instructions.

---

## 6. False Positives
- Legitimate use of file-sharing services

---

## 7. Conclusion
Unusual outbound communication may indicate C2 activity.
