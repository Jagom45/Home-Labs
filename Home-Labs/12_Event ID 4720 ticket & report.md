# Event ID 4720
- This simulates a successful attempt along with an investigation and a ticket/report

# Creating an Event ID 4720 User account created
- Open CMD in administrator mode
- Run this command: auditpol /get /subcategory:"User Account Management" to see if the auditing for it is turned on
- If it says No Auditing it means its turned off
- Run this command: auditpol /set /subcategory:"User Account Management" /success:enable
- This will turn it on
- or
- Open the run prompt with windows + R
- Click on local security policy, audit policy, audit account management
- Click on Success and the click on Apply
- Get on CMD on administrator mode
- Type in: net user test password /add
- Go to event finder and find the event ID 4720

- Date/Time - 10/3/2026 10:01:22 PM 
- Event ID - 4720
- Description - A user account was created
- Account Created - test2
- Created by - Administrator

- Subject: (Tells you who performed the action that caused the event)
	- Security ID:		cs\Administrator (Created the new test2 account)
	- Account Name:		Administrator (Name of the account)
	- Account Domain:		cs (Domain)
  - Logon ID:		0xC291B (Identifies the Administrators logon session)

- New Account: (Which account was created)
 	- Security ID:		cs\test2 (The new created account on the cs domain)
	- Account Name:		test2 (The username of the account that was created)
	- Account Domain:		cs (The domain or computer that the new account belongs to)

- Attributes:
	- SAM Account Name:	test2 (The account's Security Account Manger name)
	- Display Name:		<value not set> (Display name that is assigned to the account)
	- User Principal Name:	- (UPN User Principle Name that is assigned to the account, normally something like user@domaincom)
	- Home Directory:		<value not set> (Home directory that is configured to this account)
	- Home Drive:		<value not set> (Drive letter that is assigned to the home directory)
	- Script Path:		<value not set> (Logon script path that is assigned to this account)
	- Profile Path:		<value not set> (Windows user profile path assigned to this account)
	- User Workstations:	<value not set> (The account is not restricted to a specific workstations)
	- Password Last Set:	<never> (When the password for the newly created account was last set or changed or password change/set)
	- Account Expires:		<never> (Means account is not configured to automatically expire on a specific date)
	- Primary Group ID:	513 (This identifies the account's primary group in windows/active directory group identifiers, 513 means Domain User group, so the primary group is Domain Users)
	- Allowed To Delegate To:	- (Means no specific computer/service is listed as an allowed delegation target for this account, in other words, windows is not showing any configured resource that test2 is explicitly allowed to delegate credentials to)
	- Old UAC Value:		0x0 (The Users Account Control value before the account was created/changed, because this is a newly created account, there wasn't an existing account configuration to compare against, so windows show the previous value which is 0x0)
	- New UAC Value:		0x15 (The Users Account Control (UAC) value assigned to the newly created test2 account)
	- User Account Control: (Account control setting that windows assigned to the newly created account)
		- Account Disabled (Means it cannot be used to log on until it is enabled)
		- 'Password Not Required' - Enabled (Windows does not require a password for the account under this setting, this does not mean that no password exists)
		- 'Normal Account' - Enabled (The account is configured as a normal user account instead of a special account type)
	- User Parameters:	<value changed, but not displayed> (Means that windows is indicating that user specific parameters were changed or set, but the actual contents of those parameters are not displayed in this event)
	- SID History:		- (This means no previous Security Identifier is recorded in the SID History attribute for the new account)
	- Logon Hours:		<value not set> (Means windows is not restricting test2 to certain days or times for logging on)

- Additional Information:
	- Privileges		- (Means no additional privilegs are listed in this field for the account creation event)


- Investigation - A windows security log was investigated with an event ID of 4720. The event ID was found in event viewer with a description of A user account was created. The new user with the username of test2 was created by the account name Administrator that is associated with the cs domain.

- Analyst Determination: True Negative/ benign activity

- Conclusion - The legitimate account creation was intentional to generate a event ID 4720 for a security monitoring lab, so no evidence of unauthorized access was identified or escalation needed. No containment or remediation was need in this lab. Reason of the triggering event ID 4720 was the creation of a new account by the name test2. The case was closed and documented and marked as true negative as the creation of a new account was legitimate. 

