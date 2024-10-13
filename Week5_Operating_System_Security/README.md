Task1: Bring your own devices

1.1	Intrusive application practices
Intrusive applications are mobile apps that collect a lot of personal information from users, often without their full knowledge or consent. These apps are designed to gather various types of data, such as contact details, messages, photos, and location information. Users might unknowingly allow this data collection when they agree to the app’s terms and conditions without reading them carefully. Cybercriminals often exploit these apps to gather sensitive data for purposes like targeted advertising, selling the data, or even stealing personal or business information for espionage.

1.2	Account credential theft through phishing
Credential theft involves stealing personal information like usernames, passwords, and financial details to access online accounts or systems. This form of identity theft can use malicious software or phishing techniques. In cloud environments, identity acts as the new security boundary. Cybercriminals target these credentials to breach cloud systems and steal enterprise data. Therefore, managing access to cloud services is crucial for security, and organizations must focus on preventing credential theft to protect their cloud assets.

1.3	Outdated phones
Christoph Hebeisen, director at Lookout, a security intelligence company, warns that using a device without security patches is unsafe. He explains that critical security vulnerabilities are discovered every few weeks or months, and once a device is no longer supported, users become vulnerable to these known issues. A compromised phone can give hackers full access to everything on it, including personal and company emails, contact information, banking details, and even phone call audio. This access remains as long as the compromised device is in use.

1.4	Sensitive data transmissions
A data breach happens when someone gains unauthorized access to sensitive information, resulting in its compromise, theft, or misuse. This can occur due to various security incidents like hacking, malware, insider threats, or physical theft of devices containing the data. When sensitive information is exposed, it indicates a potential vulnerability that could lead to a data breach if not addressed promptly. Such breaches can have serious consequences for both individuals and organizations.

1.5	Brute-force attacks to unlock a phone
One of the biggest yet often ignored risks of BYOD is the use of weak passwords. Personal devices usually don’t have strict password policies, making them easy targets for brute-force attacks. Employees might choose simple passwords or reuse them across multiple accounts, including work-related ones. A Google poll revealed that one in eight adults uses the same password for all their online accounts. This habit greatly increases the risk of a security breach, as a compromised password on a personal device can give unauthorized access to sensitive company information.

1.6	Application credential storage vulnerability
This issue involves poor practices in managing and storing credentials in mobile apps. Vulnerabilities can occur when credentials like usernames, passwords, and authentication tokens are not securely handled, making them accessible to attackers.
Credentials are kept in plain text on the device’s file system, in unencrypted databases, or in unprotected shared preferences. Credentials are sent over the network without encryption (e.g., using HTTP instead of HTTPS)

1.7	Unmanaged device protection
Advise users to keep their antivirus software active and updated. Devices should have the latest technology and features to defend against new malware and attack methods. Microsoft frequently releases security intelligence and product updates. Enable encryption and firewall protection. Disk encryption safeguards data if devices are lost or stolen, while firewall protection helps prevent unwanted contact from other computers when connected to the Internet or a network. Ensure antivirus/antimalware software is installed and kept up to date on all devices. Keep devices updated with the latest operating system and application updates.

1.8	Lost or stolen data protection
Data theft involves stealing digital information from computers, servers, or electronic devices to obtain confidential information or compromise privacy. The stolen data can include bank account details, online passwords, passport numbers, driver’s license numbers, social security numbers, medical records, online subscriptions, and more. Once unauthorized individuals gain access to personal or financial information, they can delete, alter, or block access to it without the owner’s consent. Data theft typically occurs because malicious actors aim to sell the information or use it for identity theft. With enough stolen information, they can access secure accounts, set up credit cards in the victim’s name, or otherwise exploit the victim’s identity for their own benefit.

1.9	Protecting enterprise data from being inadvertently backed up to a cloud service
Cloud and SaaS applications are designed for easy sharing, which increases the risk of unintentional data exposure. For instance, an email with a shared link might be forwarded and end up outside the organization. Similarly, the person sharing the file might accidentally select the wrong email address due to autocomplete. At that point, you can only hope the mistake doesn’t lead to a security or compliance issue. Additionally, source code threats are significant. Engineers often embed user credentials in their API keys for third-party cloud services like Amazon Web Services (AWS) within the source code, which is then uploaded to repositories like GitHub. If this source code is leaked or breached, it gives attackers everything they need to hack the AWS account, including the API key and user credentials. To protect against this, implementing a Data Loss Prevention (DLP) solution is essential.

References:
https://blog.pradeo.com/the-suspect-list-part-2-intrusive-applications
https://www.crowdstrike.com/en-us/cybersecurity-101/cyberattacks/credential-theft/
https://www.cnet.com/tech/mobile/is-that-old-used-refurbished-android-phone-safe-use-what-you-should-know-security/
https://escape.tech/blog/sensitive-data-exposure/#:~:text=A%20data%20breach%20occurs%20when,of%20devices%20containing%20sensitive%20information
https://tenecom.com/risks-of-byod/#:~:text=One%20of%20the%20most%20overlooked,including%20their%20work%2Drelated%20ones
https://www.base4sec.com/research/en/N96/#:~:text=Insecure%20storage%3A%20Credentials%20are%20stored,or%20in%20unprotected%20shared%20preferences.&text=Insecure%20transmission%3A%20Credentials%20are%20sent,HTTP%20instead%20of%20HTTPS)
https://learn.microsoft.com/en-us/microsoft-365/business-premium/m365bp-managed-unmanaged-devices?view=o365-worldwide&tabs=Unmanaged
https://www.kaspersky.com/resource-center/threats/data-theft
https://paloaltonetworks.com/blog/2017/06/data-loss-prevention-prevent-accidental-data-exposure-cloud/

Task 2 Attacks on CPU execution

2.1 Retbleed is a speculative execution attack targeting x86-64 and ARM processors, including some newer Intel and AMD chips. Publicly disclosed in 2022, it is a variant of the Spectre vulnerability that exploits retpoline, a previous mitigation for speculative execution attacks. Researchers have found that mitigating Retbleed requires significant system changes, leading to performance losses of up to 14% on affected AMD CPUs and up to 39% on affected Intel CPUs running Linux.

2.2 Meltdown affects Intel x86, IBM Power, and some ARM-based microprocessors. It allows unauthorized processes to read all memory, even if they shouldn’t have access. This vulnerability impacts a wide range of systems. When it was disclosed in 2018, it affected all devices running anything but the latest patched versions of iOS, Linux, macOS, or Windows.
Mitigating this vulnerability requires changes to the operating system’s kernel code, specifically increasing the isolation of kernel memory from user-mode processes. Linux kernel developers call this measure kernel page-table isolation (KPTI). KPTI patches have been developed for Linux kernel 4.15 and have been backported to kernels 4.14.11 and 4.9.75.

2.3 Foreshadow, also known as L1 Terminal Fault (L1TF) by Intel, is a vulnerability affecting modern microprocessors. It was discovered by two independent research teams in January 2018 and publicly disclosed on August 14, 2018. This vulnerability is a speculative execution attack on Intel processors that can lead to the exposure of sensitive information stored on personal computers and third-party cloud services.
Applying software patches can help mitigate some concerns, though it’s important to balance security and performance. Companies involved in cloud computing might experience a significant reduction in their overall computing power, but researchers suggest that individual users are unlikely to notice any performance impact.

Reference 
https://en.wikipedia.org/wiki/Transient_execution_CPU_vulnerability
https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)#Mitigation
https://en.wikipedia.org/wiki/Retbleed
https://en.wikipedia.org/wiki/Foreshadow

Task 3 Securing OS

3.1 Malware and Viruses
Malware attacks can exploit weak passwords, infiltrate systems, spread across networks, and disrupt the daily operations of an organization or business. Some types of malware can lock important files, bombard you with ads, slow down your computer, or redirect you to malicious websites.
Malware defenses are structured in three layers:
1.	Prevent malware from launching or executing: Use the App Store or Gatekeeper combined with Notarization.
2.	Block malware from running on customer systems: Utilize Gatekeeper, Notarization, and XProtect.
3.	Remediate malware that has executed: Employ XProtect.
It’s the function of the OS itself and its built-in tool.

3.2 Exploiting Software Vulnerabilities
Unpatched software vulnerabilities can be exploited by attackers to gain unauthorized access, steal sensitive data, and disrupt business operations. These vulnerabilities pose significant risks, affecting everything from data integrity to regulatory compliance.
•	Apple has released security updates in macOS Mojave 10.14.5 to protect against speculative execution vulnerabilities in Intel CPUs.
•	These security issues do not affect Apple iOS devices or Apple Watch.
Previously, Apple released updates to defend against Spectre, a series of speculative execution vulnerabilities affecting devices with ARM-based and Intel CPUs. Intel has also disclosed additional Spectre vulnerabilities, known as Microarchitectural Data Sampling (MDS), which impact desktop and laptop computers with Intel CPUs, including all modern Mac computers.
It’s the function of the OS itself and its built-in tool.

3.3 Phishing and Social Engineering
Social engineering techniques are used to trick victims into revealing personal or bank card details. Attackers can store this information for future use. Social engineering often leads to data loss, credential theft, and malware or ransomware attacks. It allows attackers to gain control over resources they shouldn’t have access to.
Before running apps, installer packages, or plug-ins from outside the App Store, Gatekeeper ensures they are signed, notarized, and unaltered. iCloud Keychain helps Mac users choose stronger passwords by auto-filling information, so they don’t have to remember them all. Enabling two-factor authentication for an Apple ID prevents unauthorized access, even if someone has the password.
It’s the function of the OS itself and its built-in tool.

3.4 Drive-by Downloads
Drive-by downloads are designed to breach your device for various malicious purposes:
•	To build a botnet, infect other devices, or further compromise your system.
•	To steal your online credentials, financial information, or identity.
•	To cause trouble or harm you personally.
Whenever you download an application from a browser or an unauthorized source, macOS asks for authorization before installation and warns users about accessing malicious links or websites.
It’s the function of the OS itself and its built-in tool.

3.5 Zero-Day Exploits
Threat actors exploit zero-day vulnerabilities to gain unauthorized access to systems, stealing and potentially exposing sensitive information like personal data, intellectual property, or financial records. Although zero-day threats are challenging to defend against, a layered security approach can help mitigate their impact.
Apple has released numerous security patches to address various vulnerabilities, including a zero-day flaw that “may have been exploited” in iPhones, iPads, and Mac computers.
It’s the function of the OS itself and its built-in tool.

3.6 USB/Removable Media Attacks
One of the biggest security risks with removable media is the potential for malware and virus infections. Data breaches and loss are also major concerns when using these devices. Unauthorized access and theft are significant threats associated with removable media.
CIRCLean is an independent hardware solution designed to clean documents from untrusted USB keys or sticks. It automatically converts untrusted documents into a readable but safe format and stores these clean files on a trusted USB key or stick owned by the user.
It’s the function of the OS itself and its external tool.

3.7 Password Cracking
The most immediate consequence of unauthorized access to a user’s account is a breach of privacy, allowing unauthorized viewing, copying, or alteration of sensitive information.
iCloud Keychain helps you keep your passwords and other secure information updated across all your devices and shared with trusted individuals. It remembers your information, so you don’t have to. iCloud Keychain is protected from external attacks using advanced encryption, and Apple is transparent about how and when your data is encrypted (though the code itself is not open source). Importantly, Apple cannot see your Keychain data, ensuring your privacy.
It’s the function of the OS itself and its built-in tool.

Reference
https://www.avg.com/en/signal/what-is-malware#:~:text=Malware%20attacks%20can%20crack%20weak,redirect%20you%20to%20malicious%20websites
https://support.apple.com/en-gb/guide/security/sec469d47bd8/web
https://www.splashtop.com/blog/risks-and-vulnerabilities-of-unpatched-software#:~:text=Unpatched%20software%20vulnerabilities%20can%20be,data%20integrity%20to%20regulatory%20compliance
https://support.apple.com/en-us/103239
https://www.splunk.com/en_us/blog/learn/social-engineering-attacks.html#:~:text=These%20details%20can%20then%20be,supposed%20to%20have%20access%20to
https://simplemdm.com/blog/how-secure-are-macs/
https://www.blackberry.com/us/en/solutions/endpoint-security/ransomware-protection/drive-by-download-attack
https://discussions.apple.com/thread/8515282?sortBy=rank
https://www.ericom.com/glossary/what-is-a-zero-day-exploit/#:~:text=Loss%20of%20Sensitive%20Data%3A%20Threat,intellectual%20property%2C%20or%20financial%20records
https://www.scworld.com/news/apple-patches-zero-day-affecting-operating-systems-for-devices-macs
https://www.opswat.com/blog/removable-media#security-risks-of-removable-media
https://i.blackhat.com/USA-19/Thursday/us-19-Krstic-Behind-The-Scenes-Of-IOS-And-Mas-Security.pdf
https://discussions.apple.com/thread/250889602?answerId=251782779022&sortBy=rank#251782779022
https://www.portnox.com/cybersecurity-101/password-attack/#:~:text=Here%20are%20some%20of%20the,or%20alteration%20of%20sensitive%20information
https://support.apple.com/en-gb/guide/security/sec1c89c6f3b/web


Task4: Logging

4.1 What kind of information would be saved into following types of log files
•	Application logs
These logs are structured records of events and activities generated by software applications. They capture a wide range of information, including error messages, user interactions, system events, and application-specific data. These logs are valuable for various reasons.
•	Event logs
In computer systems, event logs capture information about both hardware and software events. These logs can be part of the operating system or specific to an application.
•	Service logs
Service logs provide diagnostic information about the resources in your environment. When logging is enabled on resources, you receive information about the resource in a log file. This information helps you analyze, optimize, and troubleshoot your resources.
•	System logs
Syslog records operating system events, including startup messages, system changes, unexpected shutdowns, errors, warnings, and other important processes. Windows, Linux, and macOS all generate syslogs.

4.2 Where in each of the common Operating Systems those logs would be stored (Windows, Mac, Linux) changes per distro, so provide in answer which you are using.
On a Mac, all logs are stored in the Console App, which can be accessed through the Applications folder.
For Windows, logs are located at C:\WINDOWS\system32\config\.
In Linux, log files are stored as plain text and can be found in the /var/log directory and its subdirectories.

4.3 What kind of threats could you notice by monitoring each log file?
•	Application logs
Access logs with the wrong credentials, application abnormal behaviour and errors in functionality. 
•	Event logs
Unknown log-in attempts, unauthorized system access and policy changes.
•	Service logs
Service abnormal behaviour due to heavy traffic or malware, and unauthorized service’s configuration changes. 
•	System logs
Hardware/software failure, kernel exploits, and unauthorised access. 

4.4 How would you go about monitoring logs on your personal computer?
First, I open the “Applications” folder through the Finder.
Then I go to the “Utilities” folder.
There, I opened the “Console” app. There I found all the logs.

References
https://newrelic.com/blog/best-practices/how-to-manage-an-application-log#:~:text=Application%20logs%20are%20structured%20records,are%20valuable%20for%20several%20reasons
https://www.crowdstrike.com/en-us/cybersecurity-101/next-gen-siem/event-logs/#:~:text=An%20event%20log%20is%20a,all%20operating%20systems%E2%80%94including%20Windows
https://docs.oracle.com/en-us/iaas/Content/General/Concepts/service_logs.htm#:~:text=Service%20logs%20provide%20diagnostic%20information,optimize%2C%20and%20troubleshoot%20your%20resources

Note: Used Microsoft Copilot for Rephrasing my lines without AI, just to correct grammer issues. There might be some similarities, therefore I've shared all references from where I got the information.  
