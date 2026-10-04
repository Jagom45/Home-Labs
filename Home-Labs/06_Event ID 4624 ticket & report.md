# Event ID 4624
- This simulates a successful attempt along with an investigation and a ticket/report

- Date/Time - 10/2/2026 8:22:32 PM 
- Hostname - WIN-F73S2MC5TMC
- Event ID - 4624
- Description - An account was successfully logged on (This event is generated when a logon session is created. It is generated on the computer that was accessed)

- Account - Administrator
- Logon Type - 2 (Interactive)
- Source IP - 127.0.0.1
- Target User: Administrator 
- Workstation - WIN-F73S2MC5TMC
- Authentication Package - Negotiate

- Investigation - A windows security log was investigated with an event ID of 4624. The event ID was found in event viewer with a description of An account was successfully logged on with a logon Type of 2 which means network. The account targeted was a Administrator account on the workstation WIN-F73S2MC5TMC.

- Analyst Determination: True Negative/ benign activity

- Conclusion - The legitimate logon was intentional to generate a event ID 4624 for a security monitoring lab, so no evidence of unauthorized access was identified or escalation needed. No containment or remediation was need in this lab. Reason for a legitimate logon was a correctly typed in username and password. The case was closed and documented and marked as false positive as the authentication success resulted from a correct username and password that was entered. 

- Personal notes

- An account was successfully logged on.

- Subject:
  	Security ID:		SYSTEM
  	Account Name:		WIN-F73S2MC5TMC$
  	Account Domain:		cs
  	Logon ID:		0x3E7

- Logon Information:
  	Logon Type:		2
  	Restricted Admin Mode:	-
  	Virtual Account:		Yes
  	Elevated Token:		Yes

- Impersonation Level:		Impersonation

- New Logon:
  	Security ID:		Font Driver Host\UMFD-1
  	Account Name:		UMFD-1
  	Account Domain:		Font Driver Host
  	Logon ID:		0xC735
  	Linked Logon ID:		0xC786
  	Network Account Name:	-
  	Network Account Domain:	-
  	Logon GUID:		{00000000-0000-0000-0000-000000000000}

- Process Information:
  	Process ID:		0x298
  	Process Name:		C:\Windows\System32\winlogon.exe

- Network Information:
  	Workstation Name:	-
  	Source Network Address:	-
  	Source Port:		-

- Detailed Authentication Information:
  	Logon Process:		Advapi  
  	Authentication Package:	Negotiate
  	Transited Services:	-
  	Package Name (NTLM only):	-
  	Key Length:		0
