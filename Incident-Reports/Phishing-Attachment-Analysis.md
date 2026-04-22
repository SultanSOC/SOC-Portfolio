# Phishing Email with Malicious Attachment – Incident Report

## Description
A suspicious email was identified targeting a user, attempting to deliver a malicious attachment disguised as a legitimate document.

---

## Evidence

- **Reply-To Email:** info.mutawamarine@mail.com  
- **Originating IP:** 192.119.71.157  
- **IP Owner:** Hostwinds LLC  
- **SPF Record:** v=spf1 include:spf.protection.outlook.com -all  
- **DMARC Record:** v=DMARC1; p=quarantine; fo=1  
- **Attachment Name:** SWT_#09674321____PDF__.CAB  
- **File Type (Actual):** CAB archive (disguised as PDF)  
- **File Hash (SHA256):**  
  2e91c533615a9bb8929ac4bb76707b2444597cc063d84a4b33525e25074fff3f  
- **File Size:** 400.26 KB  

---

## Analysis

The email exhibits multiple indicators of a phishing attack. The sender used a suspicious Reply-To address and an originating IP linked to a hosting provider (Hostwinds LLC), which is commonly abused for malicious activities.

Although SPF and DMARC records were present, this does not guarantee legitimacy, as attackers can leverage legitimate email services or misconfigurations to bypass basic email authentication checks.

The attachment is a key indicator of compromise. It appears to be a PDF file based on its name, but the actual file type is a CAB archive. This mismatch strongly suggests an attempt to deceive the recipient and bypass basic user suspicion.

Further analysis using the file hash confirmed that the attachment is malicious, indicating a high likelihood of malware delivery if executed.

---

## Conclusion

This is a confirmed phishing attack involving a disguised malicious attachment. The attacker used social engineering and file-type obfuscation techniques to trick the user into executing a malicious file.

---

## Recommendations

- Block the sender email address and associated domain  
- Remove the email from all user mailboxes  
- Block the file hash across security tools (EDR/AV)  
- Investigate if any user downloaded or executed the file  
- Educate the targeted user about phishing and malicious attachments  
