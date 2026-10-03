# Event ID 4719
- This simulates an Audit Policy Change along with an investigation and a ticket/report

- Date/Time - 10/2/2026 10:14:01 PM 
- Hostname - WIN-F73S2MC5TMC
- Event ID - 4719
- Description - System audit policy was changed
- Subject:
  - Security ID - SYSTEM (Identifies the security principal/account, SYSTEM is a build in windows account with high privilegs)
  - Account Name - WIN-F73S2MC5TMC$ (Computer account that was associated with the event)
  - Account Domain - cs (Account Domain)
  - Logon ID - 0x3E7 (Is an identifier for the windows logon session, so you can connect events that happened under the same logon session or in other windows security events)

- Audit Policy Change:
  - Category - Detailed Tracking (Broader audit policy category for process related auditing)
  - Subcategory - Process Creation (The audit policy subcategory that was changed)
  - Subcategory GUID - {0cce922b-69ae-11d9-bed3-505054503030} (GUID associated with the Process Creation audit policy subcategory, GUID stands for Globally Unique Identifier, GUID is also windows unique identifier for that specific audit policy subcategory)
  - Changes - Success Added (Success auditing was added for the Process Creation subcategory)

- Investigation - A windows security log was investigated with an event ID of 4719. The event ID was found in event viewer with a description of System audit policy was changed. The event is correlated with the workstation WIN-F73S2MC5TMC$. Success auditing was added to the Process Creation subcategory enabling windows to create Event ID 4688 when a new process is created.

- Analyst Determination: True Negative

- Conclusion - The Audit Policy Change was intentional to generate a ID 4719 event for a security monitoring lab, so no evidence of unauthorized access was identified or escalation needed. No containment or remediation was need in this lab. Reason for Audit Policy Change was the success auditing was added to the process creation subcategory. The case was closed and documented and marked as True Negative as the audit policy change resulted from an intentionally enabling 4688 logging and having to make policy changes for the process creation subcategory to success. 


You enable:
Audit Process Creation → Success
             ↓
4719
System audit policy changed
Process Creation → Success Added
             ↓
You launch Notepad
             ↓
4688
A new process has been created
