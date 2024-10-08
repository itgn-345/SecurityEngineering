Task 1: Side Channel Attacks
•	Brief explanation of what side-channel the attack uses and how
A side-channel attack doesn’t go after the program or its code directly. Instead, it gathers information or affects the system by exploiting indirect effects from the hardware or system. In simple terms, it breaks cryptography by using information that the system unintentionally leaks. Side-channel attacks involve an attacker trying to understand the state and contents of a cryptographic device. They do this by observing and analyzing information through various methods of access.

•	What systems does it affect?
Defending against side-channel attacks is challenging. These attacks are hard to detect while they are happening, often leave no trace, and usually don’t change the system’s operation. They can even be effective against air-gapped systems that are physically isolated from other networks. Moreover, side-channel attacks can target virtual machines (VMs) and cloud environments where the attacker and the target share the same physical hardware.

•	What information is leaked via the side channel?
Side channels in web application security are unintended pathways that attackers use to exploit vulnerabilities and gather sensitive information. These channels can leak data through timing differences, resource usage, error messages, or power consumption. Attackers use this leaked information to deduce critical system details. Examples include timing attacks, cache-based attacks, and network traffic analysis. To mitigate these attacks, it’s important to use secure coding practices, cryptographic algorithms resistant to side channels, and minimize timing differences.

•	Is there a documented case of it being used in a real life attack?
In early January 2018, researchers from Google and various academic institutions revealed two major vulnerabilities named Meltdown and Spectre. These flaws impacted some ARM-based processors, IBM Power processors, and Intel x86 microprocessors. Due to the widespread use of these systems, a significant portion of the world was affected by these vulnerabilities. The Meltdown exploit is quite complex. At one point, it uses a timing attack to take advantage of weaknesses in processor design. This ultimately lets attackers access all memory, including sensitive data like passwords.
•	Has it been fixed? If yes, how it was fixed?
Before the vulnerabilities were publicly disclosed, most major vendors released software patches to fix them. However, some of these updates might have slowed down systems or even caused unexpected reboots. Additionally, hardware and firmware fixes have also been made available.

References
https://en.wikipedia.org/wiki/Side-channel_attack
https://semiengineering.com/knowledge_centers/semiconductor-security/side-channel-attacks/#:~:text=Side%2Dchannel%20attacks%20are%20a,observed%20using%20different%20access%20methodologies
https://www.techtarget.com/searchsecurity/definition/side-channel-attack#:~:text=Side%2Dchannel%20attacks%20can%20even,share%20the%20same%20physical%20hardware
https://eitca.org/cybersecurity/eitc-is-wasf-web-applications-security-fundamentals/dos-phishing-and-side-channels/denial-of-service-phishing-and-side-channels/examination-review-denial-of-service-phishing-and-side-channels/what-are-side-channels-in-the-context-of-web-application-security-and-how-do-attackers-exploit-them-to-gather-sensitive-information-provide-an-example-of-a-side-channel-attack/#:~:text=Side%20channels%20in%20web%20application,error%20messages%2C%20or%20power%20consumption
https://www.comparitech.com/blog/information-security/side-channel-attack/
Note: I used Microsoft Copilot for Rephrasing.


Task 2: Slow Loris
•	How does it work?
Slowloris is a type of DDoS attack that doesn’t rely on consuming a lot of bandwidth. Instead, it ties up server resources by sending HTTP requests that are slower than usual but still look normal. Attackers exploit a feature of the HTTP protocol that allows splitting GET or POST requests into multiple packets or sessions. They target web servers by opening many connections and keeping them open for as long as possible. This is done by spreading HTTP requests across various botnet IP addresses and using multiple threads for each TCP connection. To maintain the connection, Slowloris sends HTTP headers just before the connection times out, leading to a denial of service.
 

•	Why is it unique while compared to the other high bandwith DDoS attacks?
Unlike other DDoS attacks, Slowloris uses only a few hundred slow and steady requests instead of thousands. Its detection is not about bandwidth but rather monitoring connection attempts, open connections, HTTP requests and server logs. Security teams should also check load balancers, IP connection restrictions, and other network routes.
•	What are the effects of the attack?
A single machine can take down another’s web server with minimal bandwidth and little impact on other services and ports. Slowloris works by keeping many connections to the target server open for as long as possible.
•	How can you mitigate/prevent the effects of the attack?
Here are some ways to protect against attacks:
1.	Restrict the number of connections each IP can make.
2.	Set a higher minimum transfer speed for connections.
3.	Limit how long a client can stay connected.
4.	Increase the maximum number of clients the server can handle.
5.	Use strong cloud mitigation services, configure effective load balancers, deploy web application firewalls (WAFs), apply virtual patches, and limit the number of requests from each source.

•	Are there any notable instances of this style of attack being performed?
In 2009, Iran claimed that the US used Slowloris attacks on its government websites, causing major disruptions for several weeks. Similarly, in 2018, a group of hackers called MoneyTaker launched a Slowloris attack on several Russian banks, making their websites inaccessible.



References
https://www.akamai.com/glossary/what-is-a-slowloris-ddos-attack#:~:text=Slowloris%20DDoS%20Attacks%20Explained&text=This%20type%20of%20cyber%20abuse,HTTP%20connections%20per%20connected%20session
https://en.wikipedia.org/wiki/Slowloris_(cyber_attack)#:~:text=Slowloris%20is%20a%20type%20of,on%20unrelated%20services%20and%20ports.&text=Slowloris%20tries%20to%20keep%20many,open%20as%20long%20as%20possible
https://www.indusface.com/blog/what-is-slowloris/#:~:text=Here%20are%20a%20few%20examples,by%20the%20hacker%20group%20LulzSec
Note: I used Microsoft Copilot for Rephrasing.

Task 3 Burp Suit Introduction
Subtask 1: Intercepting

Editable Request: 
GET / HTTP/1.1
Host: localhost
sec-ch-ua: "Not;A=Brand";v="24", "Chromium";v="128"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "macOS"
Accept-Language: en-US,en;q=0.9
Upgrade-Insecure-Requests: 1
User-Agent: Abubaker Umer (Table Lamp)
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Sec-Fetch-Site: none
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

Subtask 2: Repeater
After changing the security level from low to medium, I’ve observed that instead of a sequence-wise increase in the session ID, generating new cookies each POST request provides a strong randomised session ID every time. 
 

 

Subtask 3: Intruder
 
 
I’ve observed that two brute force attacks were successful, as shown below in the attachments.
 
 


Subtask 4: Decoder
Encode as URL:
 
Encode as HTML:
 
Encode as Hex:
 
Encode as Binary:
 

Smart Decode: 
 


Subtask 5: thc-hydra
 
 
The brute force attack too 8 minutes to get the original password “bake”.
Below is the command:
docker run --network="host" vanhauser/hydra -V -f -I -l admin -x 1:4:a "http-get-form://localhost/vulnerabilities/brute/:username=^USER^&password=^PASS^&Login=Login:H=Cookie:PHPSESSID=5nk9sile2ocotach62icidsm03; security=low:F=Username and/or password incorrect."
