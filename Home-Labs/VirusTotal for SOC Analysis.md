# Lab purpose
- Use VirusTotal to analyze files and URLs for the presence of malware and other security threats

# VirusTotal
- Go to: https://www.virustotal.com/gui/home/upload
- Go to https://vx-underground.org/
- Vx underground is a website that collects and archives various malware, exploits and other malicious software
- This site is a repository for these type of software providing acess to these type of materials for research and analysis purpose
- Pick a sample and upload it to VirusTotal
- Once uploaded Virustotal gives you more information like hashes, size, and type
- In the relations section dynamic analysis of the executable is performed and we can see the contacted domains, internet protocol addresses and even the files that where dropped by the executable on the system
- You can see things like the different IP addresses that it tried to contact after the executable ran, in this case 51 different IP addresses where contacted
- You can see the different files that where dropped on the affected system, in this case 379 filfes where dropped on the system
- The graphical summary provides a nice overview of the malicious file effects on the system

# Conclusion
- Using Virustotal for analysis on files that could potentially contain malware and see the different effects it could have on a system provides a way how the malicious file behavies and a way
