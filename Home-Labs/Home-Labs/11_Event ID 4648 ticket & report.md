# Event ID 4624
- This simulates a successful attempt along with an investigation and a ticket/report

- Date/Time - 10/3/2026 7:50:04 PM 
- Hostname - WIN-F73S2MC5TMC
- Event ID - 4624
- Description - A logon was attempted using explicit credentials. (This does not mean the logon was successful)

- Subject:
	- Security ID:		SYSTEM (A highly privileged windows operating system account)
	- Account Name:		WIN-F73S2MC5TMC$ (Computer's account)
	- Account Domain:		cs (Domain that it belongs to)
	- Logon ID:		0x3E7 (The logon ID identifies the logon session)
	- Logon GUID:		{00000000-0000-0000-0000-000000000000} (The Globally Unique Identifier, an identifier that windows can use to correlate authentication related events)

- Account Whose Credentials Were Used:
	- Account Name:		WIN-F73S2MC5TMC$ (The credentials being explicitly used belonged to the computer account WIN-F73S2MC5TMC$)
	- Account Domain:		CS.ORG (Which domain the account whose WIN-F73S2MC5TMC$ belonged to) (CS.ORG\WIN-F73S2MC5TMC$)
	- Logon GUID:		{eb26a2b9-edf1-8845-899b-fd7bbacec0f0} (Globally Unique Identifier associated with the logon/authentication activity)

- Target Server:
	- Target Server Name:	win-f73s2mc5tmc$ (Means which server/computer the credentials were being used to access) or (the computer/server the credentials were being used against)
	- Additional Information:	win-f73s2mc5tmc$ (Provides additional information about the target invovled in the credential use attempt)

- Process Information:
	- Process ID:		0x258c (Means the Process ID and it identifies the specific process that generated or was associated with this event, 0x258c is the identifier windows gave to the process involved in the event and its written in hexadecimal under event viewer, this is the process that was involved in the in the event)
	- Process Name:		C:\Windows\System32\taskhostw.exe (taskhostw.exe was given the process ID of 0x258c, this also means the windows process that was involved in the credential use attemtp)

- Network Information:
	- Network Address: - (The network address from which the credential use attempt originated)
	- Port: - (Means which network port was associated with the activity) (- no network address recorded)

This event is generated when a process attempts to log on an account by explicitly specifying that account’s credentials.  This most commonly occurs in batch-type configurations such as scheduled tasks, or when using the RUNAS command.

- Investigation - A windows security log was investigated with an event ID of 4648. The event ID was found in event viewer with a description of a logon was attempted using explicit credentials. The the credentials used was from the account name of WIN-F73S2MC5TMC$ that belonged to the cs.org.

- Analyst Determination: True Negative/ benign activity

- Conclusion - The legitimate logon was intentional to generate a event ID 4648 for a security monitoring lab, so no evidence of unauthorized access was identified or escalation needed. No containment or remediation was need in this lab. Reason for using explicit credentials was to generated an event ID of 4648. The case was closed and documented and marked as True Negative as the attempt to log on by providing explicit credentials was legitimate and resulted from a correct username and password that was entered. 

