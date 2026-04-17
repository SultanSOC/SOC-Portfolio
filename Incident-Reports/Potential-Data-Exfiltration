# Potential Data Exfiltration – False Positive

## Description
An SIEM alert flagged large data transfer from an internal device to an external domain.

## Evidence
- Source IP: 192.168.45.66
- Destination: zoom.us
- Data Sent: 5.8 GB
- Network: Meeting room

## Analysis
- Large data transfer detected
- Destination is trusted (Zoom)
- Activity matches normal video conferencing usage

## Conclusion 
False Positive – Legitimate Zoom activity

## Recommendations
- Tune SIEM rule
- Whitelist trusted domains like Zoom
- Reduce false alerts
