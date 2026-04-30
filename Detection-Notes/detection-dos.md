# Detection Note: Denial of Service (DoS)

## 1. Overview
A DoS attack floods a system with requests to make it unavailable.

---

## 2. Why It Matters
Causes service disruption.

---

## 3. Key Indicators
- High number of requests
- Multiple IPs
- 503 server errors
- Repeated requests to same endpoint

---

## 4. Detection Logic
Monitor traffic spikes and repeated access to resource-heavy endpoints.

---

## 5. Example Scenario
Multiple requests to /search causing server overload.

---

## 6. False Positives
- Legitimate traffic spikes (e.g., sales events)

---

## 7. Conclusion
Unusual traffic patterns may indicate DoS activity.
