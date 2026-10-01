# Lab purpose
- Use static analysis of phishing emails using VirusTotal and AbuselPDB
- Static analysis of phishing email can help identify potential malicious emails

# Static analysis with AbuselPDB
- Obtain the IP address from the email from the Email Header Analysis Basic lab
- Go to https://www.abuseipdb.com/ and type in the IP address found in the email header
- AbuselPDB tells us that the IP address found in the email has been reported with the following: Email Spam, Spoofing, Brute-Force, the person who reported it, the Timestamps and comment left by those people which include things like spf and dkim fail or email not accepted due to domain's DMARC policy

# Static analysis with VirusTotal
- Go to https://www.virustotal.com/gui/home/upload
- If the phishing email contains a URL, insert the URL under the URL tab
- In this case I will be using the URL: https://phishing-url-example.com@is.gd/rYvd5e
- Virustotal tells use that Chong Lua Dao and Gridinsoft has labeled this URL as Malicious and Phishing
- It also gives us an IP address of 172.67.83.132
- Go back to AbuselPDB and insert that IP address and check the results
- The results come back with multiple categories like: Phishing, Web Spam, Email Spam, Spoofing, Fraud Order and others

# Conclusion
- Performing static analysis can help detect phishing email using tools like VirusTotal and AbuselPDB
- Those tools can also identify potentially malicious emails and URLS

# Actions
- You can use Outlook to block emails that contain that URL
- To make a rule to block emails that contain that specific URL go to, click on Mail, then rules, then add new rule, give it a name like Block phishing URL, under add a condition, select Message body includes or body includes, insert the malicious URL, under add an action, select Delete or move to Spam folder, click save
