# Phishing Email Report
-This file contains the ticket/incident report for a Phishing Email Lab

Incident/Ticket ID: 1

Alert/Detection: Sally receives a suspicious email that says to reset her email and reports it to IT to examine to investige the message

Date/Time: 9/30/26 10:10PM

Severity: Low

Affected Hosts: None as Sally did not click on any links yet

Affected Users: Sally is the target even though there is no evidence of compromise

Source IP/: 101.99.94.116 and identified from the email's reciever header as part of the message's SMTP path

Detection Alert: Sally reported the suspicious email

Initial Alert: A suspicious password resetting email containing an urgent request to reset the password and containing a link to change the user's email password

Investigation: Analyzed the email's .eml file and examined the email headers, including the recieved, From-To/Return-Path, SPF, DKIM, and DMARC information. The sending IP was compared against legitimate mail infrastructure associated with the claimed sender domain. There was inconsistencies between the claimed sender and the observed SMTP infrastrucutre, indicating that the email was spooefed. The email also contained an urgency to do a password reset and click on the link.

Raw Event Evidence: No security event created, but the focus was on email-header analysis. The original header and the .eml information was teh primary evidence

IoC Analyis: Identified several indicators like the sending IP address, sender/domain information, SMTP routing information and difference between the claimed sender and observed mail infrastructure and a suspecial link in the body of the email. Header analysis indicated that the email did not originate from the legitimate mail inftrastructure that the sender claim to be from.

MITRE ATTACK Mapping: The email demonstrated characteristics of a phishing attack, T1566 as Phishing Email with technique as T1566.002 for spearphisihg link as the email contained a link

Scope/Impact: Low, no link was clicked on, no evidence of account compromise, no malware executed or endpoing compromise

Containment: Prserve the suspicous email for investigation, prevent the recipient from clicking on the suspicious link, you can also move or quarantine the email

Remeditaiton: Block the identified sender or malicious domain where the email originated from and create an email filtering rule based on characteristics of the phishing email to move similar emails to junk or quarantine folder, also continue the monitoring of similar phishing messages targeting other users

Escalation: No escalation required because no user interacted with the link and no evidence of compromise was identified

Final Disposition: Incident contained and closed, the email was investigated through email header analysis, including the sender information, and SMTP routing. It was identified that the email was a spoofed message. No evidence or system compromise was identified, the suspicious email with the suspecious link was detected and investegated with TotalVirus and verifiting that the link was a phishing link to steal credentials. Email rule was created to prevent future similar emails like that to be quarantined or moved to junk folder. Similar messages should be monitored to see if additional users where also targted.


Analyst Notes: Email-header analysis showed things like email headers and the SMTP path. The sending IP address did not correspond with the legitimate mail infrastructure and the claimed sender domain, showing characterisitcs of evidence of a spoofed email. The presence of an urgent password-reset request and an email that says to click on this link was also evidence of a phishing email.

Lesson Learned/Detection Improvements: User awarness and reporting suspecious emails can allow analysis to investigate those emails before the user interacts with malicious link. Email filters can be used to block future emails with similar characteristics of phishing emails that contain suspecious URL's, block malicious sender and domains. Also authenciation failures, SPF, and DMARC should be monitored to help idenfity spoofed email. Similar messages should be monitored to see if additional users where also targted.












