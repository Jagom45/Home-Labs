# Event ID 4726
- This simulates a User Account Deleted along with an investigation and a ticket/report

# Turning on auditing for Event ID 4726
- Press Windows + R
- Type in secpol.msc and press enter
- Click on local policies, click on audit policy
- Double click on account management auditing
- Click on success and then click on apply and then press okay

# Creating an Event ID 4726 User Account Deleted
- Type in run in the search bar
- Type in dsa.msc and press enter
- You can make a new account, left click on the user folder
- For first name type in: test2
- For last name type in: test2
- For full name type in: test2
- For logon name type in: test2
- On the temporary account password page uncheck everything
- Enter the password as password and click on next
- Click on finish
- Click on the user that you just created and left click on it and select Delete
- On the Active Directory Domain Services click on yes
- Go to the event viewer and find the Event ID 4726




- A user account was deleted. (This is the description)

- Subject: ( This section identifies the security principal that performed the action recorded by Event ID 4726)
	- Security ID:		cs\Administrator (Identifies the security principle that performed the deletion)
	- Account Name:		Administrator (The user account that performed the action)
	- Account Domain:		cs (The domain that Administrator belongs too)
	- Logon ID:		0xC291B (The hexadecimal identifier that represents the specific logon session in which the account deletion was performed, associated with the session when the deletion was performed)

- Target Account: (This section identifies the user account that was affected by the deletion.)
	- Security ID:		S-1-5-21-353739892-4176304805-2976134450-2102 (The Security Identifier SID of the user account that was deleted)
	- Account Name:		test2 (The username of the account that was deleted)
	- Account Domain:		cs (The domain that the deleted account belonged to)

- Additional Information: (This is a section containing extra information Windows may provide about the account-deletion operation.)
	- Privileges	- (Means that Windows did not record any specific privileges associated with this event)


- Date/Time - 10/3/2026 11:52:52 PM 
- Event ID - 4720
- Description - A user account was deleted
- Account Created - test2
- Created by - Administrator

- Investigation - A windows security log was investigated with an event ID of 4720 The event ID was found in event viewer with a description of a user account was deleted. The Administrator account deleted a account with the username of test2.

- Analyst Determination: True Negative/ benign activity

- Conclusion - The account was deleted intentionally to generate a event ID 4726 for a security monitoring lab, so no evidence of unauthorized access was identified or escalation needed. No containment or remediation was need in this lab. Reason of the triggering event ID was the deletion of the account test2 was deleted by the account Administrator. The case was closed and documented and marked as true negative as the deletion of the account was legitimate. 


...._Event ID .... ticket & report.md


