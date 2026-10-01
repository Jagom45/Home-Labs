# Lab Purpose
- VirusTotal can be used to analyze files and URL's for known signature of malicious activities

# VirusTotal
- Upload the previous file into VirusTotal
- Go to the behavior section of VirusTotal
- Select all of the options available
- Details and its capabilities is given to why it things its a malicious file
- In this case, Execution TA0002 was giving, creates COM task schedule object often to register a task for autoStart along with other things
- Along with that an explanation can be found by hovering over the tactic that was given
- In this case it says that the adversary is trying to run malicious code and you can view it in MITRE ATT&CK as well

# Using a malicious URL
- Upload a malicious URL link to VirusTotal, in this case this link will be used: br-icloud.com.br
- Go to the HTTP response section under the Details section
- In this case you can see that the website is still functional as the Status Code is still 200 along with the body lengh of 2.93kb and the content type being an image/png rather than HTML or text/html
- Under the Network Requests/HTTPs Transactions is says that 15 out of 92 of the security vendors flagged these IoC's as malicious

# Indicators of Compromise by using a Hash
- You can also use the hash of a file and upload it to VirusTotal
- Go to this site and download HashCalc: https://sourceforge.net/projects/hashcalc/
- Use the program to create a hash of a file and upload it to VirustTotal under the search tab
- In this case the file came out as malicous with 53/70 score with things like being identified as a Trojan under threat categories

# Conclusion
- VirusTotal is a great tool to see if files or URL are malicious, you can analyze the behavior of malicious executables and analyze IoC's
- With VirusTotal you can use its various antivirus engines and use its database of known signatures of malicious activates to perform analysis on files and URLs to prevent potential security threats
