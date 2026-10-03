# Event ID 4625 Ticket
- This simulates a failed attempt along with an investigation and a ticket/report

Date/Time - 10/2/2026 8:22:23 PM 
Hostname - WIN-F73S2MC5TMC
Event ID - 4625
Description - An account failed to log on (This event is generated when a logon request fails. It is generated on the computer where access was attempted. (Unknown user name or bad password)
)
Account - Administrator
Logon Type - 2
Source IP - 127.0.0.1
Target User: Administrator 
Workstation - WIN-F73S2MC5TMC
Authentication Package - Negotiate

- Investigation - A windows security log was investigated with an event ID of 4625. The event ID was found in event viewer with a description of An account failed to log on with a logon Type of 2 which means interactive or logon locally. The account targeted was a Administrator account on the workstation WIN-F73S2MC5TMC.

- Analyst Determination: False positive

Conclusion - The failed logon was intentional to generate a event ID 4625 for a security monitoring lab, so no evidence of unauthorized access was identified or escalation needed. No containment or remediation was need in this lab. Reason for failure was a bad password. The case was closed and documented and marked as false positive as the authentication failure resulted from an intentionally wrong password that was entered. 
