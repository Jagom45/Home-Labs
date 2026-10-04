# Event ID 4672

- This simulates an Special privileges assigned to new logon along with an investigation and a ticket/report

- Date/Time - 10/2/2026 10:14:01 PM 
- Hostname - WIN-F73S2MC5TMC$
- Event ID - 4672
- Description - Special privileges assigned to new logon

- Subject:
  -	Security ID - SYSTEM
  -	Account Name - SYSTEM
  -	Account Domain - NT AUTHORITY
  - Logon ID - 0x3E7 (Can be used to correlate other security events with 0x3E7) (This also is corralated with event ID 4624 because a logon was successful and then special privileges where assigned to that logon session which is the administrator account with the Logon ID of 0x3E7)
- Task Category - Special Logon

- Privileges:
  - SeAssignPrimaryTokenPrivilege (This privilege allows a process to replace the primary token associated with a process, which is being assigned to NT Authority/SYSTEM)
  -	 SeTcbPrivilege (Windows privilege that allows a process to operate with a very high level of trust from the operation system and interact with security mechanisms in ways that a normal user account can't)
  -  SeSecurityPrivilege (This privilege allows account/process to perform certain security related operaitons including operations in the security event log and auditing and security settings)
  -	 SeTakeOwnershipPrivilege (Allows a privileged account to take ownership of securable objects, like files, folders, registry keys, or windows resources, even when it is not the current owner of it)
  -	 SeLoadDriverPrivilege (Allows a privileged account to load and unload device drivers, drivers operate at a very low level in windows)
  -	 SeBackupPrivilege (Allows a privileged account to bypass normal file and folder permissions when performing backup operations, and example of this would a backup process may need to read files that the account normally wouldn't have permission to acess)
  -	 SeRestorePrivilege (Allows a privileged account to bypass certain normal files and registry permissions when restoring data or objects, helps privileged process read/access (data backups) and write/restore protected data)
  -	 SeDebugPrivilege (Allows a highly privileged process to debug or inspect a process that it would not normally have permission to access)
  -	 SeAuditPrivilege (Allows a process to generate security audit events in the windows security logs)
  -	 SeSystemEnvironmentPrivilege (Allows a privileged process to modify certain system environments variables stored in firmware such as UEFI/BIOS environment)
  -	 SeImpersonatePrivilege (Allows a process to impersonate the security context of another user or process under certain conditions)
  -	SeDelegateSessionUserImpersonatePrivilege (Allows a privileged process to delegate or impersonate a user's security context within a session under specific windows conditions )

- Investigation - A windows security log was investigated with an event ID of 4672. The event ID was found in event viewer with a description of Special privileges assigned to new logon. The event is correlated with the workstation WIN-F73S2MC5TMC$. A series of different very high privileges where assigned to the NT Authority/SYSTEM)

- Analyst Determination: True Negative

- Conclusion - The special privileges assigned to new logon with an Administrator account was intentional to generate a ID 4672 event for a security monitoring lab, so no evidence of unauthorized access was identified or escalation needed. No containment or remediation was need in this lab. Reason for Special privileges assigned to new logon was the very high level privileges being assigned to NT Authority/SYTEM. The case was closed and documented and marked as True Negative as the audit policy change resulted from an intentionally .



4624
→ successful logon
→ Logon Type 2
→ Elevated Token: Yes
→ Logon ID 0x3E7

4672
→ special privileges assigned
→ same Logon ID 0x3E7
→ SYSTEM receives powerful privileges
