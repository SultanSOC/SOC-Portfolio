# Detection Note: LOLBins Abuse (certutil.exe)

## 1. Overview
Attackers use legitimate system tools to perform malicious actions.

---

## 2. Why It Matters
Helps attackers evade detection.

---

## 3. Key Indicators
- certutil.exe making network connections
- File download from external URL
- Suspicious command-line usage

---

## 4. Detection Logic
Monitor process creation logs for certutil usage with URLs.

---

## 5. Example Scenario
certutil downloads malicious file from external domain.

---

## 6. False Positives
- IT administrators using tools legitimately

---

## 7. Conclusion
Unusual usage of system tools may indicate compromise.
