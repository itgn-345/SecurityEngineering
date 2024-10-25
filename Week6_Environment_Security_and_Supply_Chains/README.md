Task 1: Secure Running Environment?
Virtualization is a technology that allows multiple operating systems to run on a single physical machine by creating virtual machines (VMs). Each VM operates independently, providing strong security through isolation, meaning one compromised VM usually can’t affect others or the host system. This isolation is useful for environments where strict separation of tasks is required. However, virtualization's limitations include high resource usage because each VM runs its full OS, consuming significant memory and processing power. There’s also the risk of hypervisor attacks, where compromising the hypervisor could lead to control over all VMs on the host.
Containers, on the other hand, share the host system's kernel and are more lightweight compared to VMs. Containers package an application and its dependencies into a single unit, enabling consistent performance across different environments. This makes containers ideal for efficient resource utilisation and fast deployment. However, containers' security is weaker than VMs because they share the host OS kernel. A kernel vulnerability could allow a compromised container to affect the host or other containers. Despite this, containers are widely used in environments prioritising speed and scalability over strict isolation, and security can be enhanced with proper configurations like namespaces and control groups.
In terms of security:
•	Virtualization offers stronger isolation because each VM has its own OS, making cross-VM breaches difficult. However, it is resource-intensive and may be vulnerable at the hypervisor level.
•	Containers are more efficient and faster to deploy but offer weaker isolation, as they share the host's kernel. A compromised kernel could lead to system-wide breaches.
Both technologies serve different use cases, and security considerations should be based on the specific requirements of the deployment environment.

References:
https://www.relianoid.com/blog/virtualization-security-issues-and-risks/
https://www.profsandhu.com/cs6393_s14/csur_virt_2013.pdf
https://cyberexperts.com/virtualization-security/
https://www.cloud4c.com/blogs/container-security-management-top-5-checks-and-best-practices
https://sysdig.com/blog/container-security-best-practices/
https://www.redhat.com/en/resources/guide-nist-compliance-container-environments-detail

Task 2: Supply Chain Attacks
Introduction: In modern software development, securing the supply chain is a critical challenge due to the involvement of multiple third-party actors. For ABC Software Company, their supply chain includes their employees, contractual coders from Company C, software audits performed by Company D, and internal tools hosted by Company E. Each of these entities plays a significant role in the integrity and security of the final product. This report outlines specific actions and security measures ABC can implement to mitigate risks within its supply chain. These measures will focus on ensuring that none of the actors involved compromise the software's security through malicious actions or vulnerabilities.
Actors in the Supply Chain and Concerns:
1.	ABC’s InHouse Employees: ABC's internal employees are responsible for creating the software. Insiders can be a significant risk, intentionally or through negligence, so robust internal security measures are crucial. By implementing User Behavioral Analytics (UBA), the company can monitor employee behaviour for any unusual activity, such as unauthorized access to sensitive parts of the codebase or excessive file downloads. UBA detects deviations from normal employee behaviour and can provide early warnings of insider threats or compromised accounts.
While UBA can flag suspicious activity, it requires careful tuning to avoid false positives, which could lead to unnecessary investigations. ABC will also need to address privacy concerns to prevent employee distrust.
2.	Company C (Contractual Coders): Contractual coders from Company C represent a significant risk, as they may not be as loyal or trustworthy as in-house employees. To secure the code being developed by these external contributors, Endpoint Detection and Response (EDR) should be deployed. EDR solutions continuously monitor endpoints, detect unusual activities, and respond to potential threats in real-time. ABC can ensure that all external coders use secured environments monitored by EDR, which will allow them to detect any malware insertion, backdoors, or unauthorized data access.
Managing and deploying EDR for contractual coders might require setting up isolated virtual environments. ABC must also ensure compliance from Company C to use approved tools and processes, which may add complexity to contracts and collaboration processes.
 

3.	Company D (Audit): Company D audits the software produced by ABC. Since auditors need access to the codebase, they could unknowingly introduce vulnerabilities or act maliciously. To mitigate this, ABC can use Trusted Platform Modules (TPMs) to verify the integrity of the software and ensure that any changes made by auditors are legitimate. TPMs store cryptographic keys securely and can verify whether the software has been tampered with. ABC should require Company D to follow strict protocols for accessing and auditing the codebase, with TPMs providing a final verification check before the product is shipped.
TPMs may introduce additional delays, as the cryptographic verification process takes time. Additionally, TPMs need to be integrated into the development and audit environments, which could require extra technical resources.
4.	Company E (Hosting Internal Tools): Company E hosts internal tools for ABC. Hosting platforms represent a critical point of vulnerability, as they could be exploited through compromised tools or data leaks. Implementing Network Detection and Response (NDR) will help ABC monitor and detect any unusual network activity between ABC and Company E’s hosted services. NDR solutions can identify and block malicious traffic, such as external access attempts or lateral movement within ABC’s infrastructure. NDR systems require continuous monitoring and adjustment to be effective, and they generate large volumes of data. ABC will need dedicated resources to analyze this data and respond to potential incidents quickly.
 

References:
https://pentest-tools.com/blog/supply-chain-attack
https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-161r1.pdf
https://en.wikipedia.org/wiki/Supply_chain_attack
https://www.crowdstrike.com/wp-content/uploads/2022/03/crowdstrike-edr-and-ndr-data-sheet.pdf
https://exeon.com/blog/the-importance-of-an-ndr-solution-to-early-detect-supply-chain-attacks-in-corporate-networks
https://amplitude.com/glossary/terms/user-behavior-analytic
https://www.kuppingercole.com/research/lc80489/network-detection-response-ndr
https://gridinsoft.com/edr
https://en.wikipedia.org/wiki/Total_productive_maintenance#:~:text=Total%20productive%20maintenance%20(TPM)%20started,operating%20cost%20to%20an%20organization
