# Event ID 4688 Ticket
- This simulates a new process being created along with an investigation and a ticket/report
- Example of this can be powershell.exe, cmd.exe, whoami.exe, mimikatze.exe

# Enabling 4688 logging
- Press Windows + R and type in secpol.msc and press enter
- Advanced Audit Policy Configuration → System Audit Policies → Detailed Tracking
- Double click on Audit Process Creation, click on the check box for Configure the following audit events and then click on the check box for Success
- Doing this creates an event ID of 4719 Audit Policy Change

- Date/Time - 10/2/2026 10:15:10 PM 
- Hostname - WIN-F73S2MC5TMC
- Event ID - 4688
- Description - A new process has been created 
- Account Name - Administrator (The new process was created under Administrator account)
- New Process ID: 0xb38 (Identifier that windows assigned to the new process, PID of notepad is 0xb38)
- New Process Name:	C:\Windows\System32\notepad.exe
- Token Elevation Type - TokenElevationTypeDefault(1) (1 stands for the process is running with the default token)
- Mandatory Label - Mandatory Label\High Mandatory Level (High Mandatory means the process is operating at the High integrity level)
-	Creator Process ID:	0x1ec8 (The process that started Notepad, so the PID of CMD is 0x1ec8)
- Creator Process Name - C:\Windows\System32\cmd.exe (What created Notepad) (cmd.exe = parent process & notepade.exe = child process)
- Note: 0x1ec8 and 0xb38 change as they are just instances that where launched and are in hexadecimal. If the same programs get launched again a new PID will be assigned to it by windows this number can be found in task manager as well. In event viewer the hexadecimal number gets used which are the numerical value of the hexadecimal numbers.
  
- Investigation - A windows security log was investigated with an event ID of 4688. The event ID was found in event viewer with a description of A new process has been created. The new process was created on the Administrator account. There is evidence that CMD.exe was used to launch notepad.exe. CMD is the parent process and notepad is the child process. The PID of CMD is 0x1ec8 and the notepad PID is 0xb38.

- Analyst Determination: True Negative/benign activity

- Conclusion - The new process was intentional to generate a event ID 4688 for a security monitoring lab, so no evidence of unauthorized access was identified or escalation needed. No containment or remediation was need in this lab. Reason for the generated event was because notepad.exe was created by CMD.exe. The case was closed and documented and marked as True Negative as the new process resulted from an intentionally making a new process which was notepad.exe with CMD.exe. 
