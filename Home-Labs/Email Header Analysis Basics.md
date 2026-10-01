# Lab purpose
- Understand basic email header analysis

Email Header Analysis Basics
- Email head analysis examines the metadata in the email header section to see the origin, path and contents of an email message
- Email analysis helps identify and prevent phishing attacks, detect spam emails, identify the source of fraudulent emails, and investigate cybercrimes]
- Email headers can contain the senders IP address, email client, email servers involved in the transaction, and time stamps of the message

# Email Header breakdown
- Received - This field indicates the email servers the message passed through to get to the recipient. Each servers IP address and hostname are listed including the time stamps
- DKIM - DomainKeys Identified Mail is a security protocol that an organization uses to sign its outgoing email messages with a digital signature. The DKIM signature can be used to verify the message authenticity and check if the email was tampered with or forged in transit
- SPF - Sender Policy Framework is a security protocol that allows email servers to verify that incoming email messages are coming from authorized sources. SPF can also be used to detect spoofed or fraudulent emails
- DMARC - Domain-based Message Authentication, Reporting, and Conformance is a security protocol that built on DKIM and SPF to provide additional protection against email fraud. DMARC allows domain owners to specify how they want their emails handled if they fail authentication checks. So with DMARC policy you can determine how the email is treated and weather it is trustworthy.

# Accessing the Email Header
- Go to the email that you want to inspect
- Click on the 3 dots and then click on download email
- Open the downloaded file with the extension .eml with any notebook application

# Checking if the Email was sent from the correct SMTP Server
- By checking the received field to see the path followed, we get an IP address of 101.99.94.116 for the IP server
- By checking the sender field, we see that it came from the domain Letsdefend.io
- We can use mxtoolbox.com to show you the MX servers used by the domain
- After checking with mxtoolbox.com, we can see that there is no IP listed as 101.99.94.116
- This confirms that that the email did not come from the original address but was spoofed

# Are the Data for the field From and Return Path/Reply To the same?
- In normal cases the sender of the email and the person receiving the response will be the same
- In a phishing email, the fields will be different, an example of that would be:
- A bad actor uses the same last name of someone who works in the IT department at company ABC, that person sends an email to company ABC and Sally receives the email and tells Sally that she needs to click on this link to reset her password and comply with company password policy and that its very urgent for her to comply with it, but Sally is not expecting this email yet but until 2 months later
- The bad actor will put the actual employee who works in the IT department in the Reply-to field so that the fake email address does not stand out in case of replying to the email
- You can check in the notebook application that the fields are different

# Conclusion
- The email is a phishing email, there are instances of urgency in the email to comply with a demand to change a password, the headers also help see that the email was spoofed
- Email headers analysis helps identify and prevent phishing attack, and detect spam email

# Actions
- You can use outlook to block the exact sender
- You can use outlook to block the domain where the email come from
- You can use outlook to create an rules based on the email characteristics like working or subject line
- To create the rule, go to settings, to to mail, go to add new rule, give the rule a name, under add a condition choose subject includes, add the subject line of the phishing email, under add an action, choose move to junk email and save the rule
