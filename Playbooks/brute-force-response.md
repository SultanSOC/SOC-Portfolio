# Playbook: Brute Force Response

## 1. Validate the Alert
- Review failed login attempts
- Identify the affected account
- Check the source IP address

---

## 2. Investigate
- Look for multiple failed logins followed by a successful login
- Check if other accounts are being targeted
- Review login locations and timestamps

---

## 3. Contain
If malicious:
- Block the source IP if appropriate
- Lock or disable the affected account
- Force a password reset if compromise is suspected

---

## 4. Escalate
Escalate if:
- A successful login follows multiple failed attempts
- Multiple accounts are targeted
- Privileged accounts are involved
- Suspicious login locations or impossible travel are detected

---

## 5. Recover
- Confirm the account is secure
- Monitor for additional login attempts
- Advise the user to enable MFA if available
