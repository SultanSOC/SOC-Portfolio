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

The email looks suspicious.

The IP address belongs to a hosting company, which attackers often use.

Even though SPF and DMARC exist, this does not mean the email is safe.

The attachment is the main problem. It looks like a PDF, but it is actually a CAB file. This is a trick to fool the user.

The file hash check shows the file is malicious.

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
