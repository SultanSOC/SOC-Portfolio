# Domain Enumeration Activity with Suspected Reverse Shell

## Description
A SIEM alert detected a spike in domain discovery commands on a critical server, indicating potential post-exploitation activity.

## Evidence
- Host: DMZ-MSEXCHANGE-2013
- Time: 19:56
- User: NT AUTHORITY\SYSTEM
- Commands:
  - whoami /priv
  - net group "Domain Admins" /domain
  - nltest
- Process Tree:
  - w3wp.exe → revshell.exe → cmd.exe

## Analysis
The observed commands indicate domain enumeration activity, commonly performed by attackers after initial access.  
The process tree shows a web server process spawning a suspicious executable (revshell.exe), which then launched a command shell.  

This behavior strongly suggests that the server has been exploited.

## Conclusion
True Positive – The activity indicates a compromised system with a likely reverse shell and post-exploitation behavior.

## Recommendation
- Immediately isolate the affected host from the network
- Initiate incident response procedures
- Investigate the source of the compromise
- Remove malicious files (revshell.exe).
