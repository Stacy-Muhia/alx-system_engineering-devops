****POSTMORTEM PROJECT****

_Any software system will eventually fail, and that failure can come stem from a wide range of possible factors: bugs, traffic spikes, security issues, hardware failures, natural disasters, human error
After any outage a **postmortem**  a tool widely used in the tech industry is impelemented.A summary that has two main goals_

1.To provide the rest of the company’s employees easy access to information detailing the cause of the outage. Often outages can have a huge impact on a company, so managers and executives have to understand what happened and how it will impact their work.

2. And to ensure that the root cause(s) of the outage has been discovered and that measures are taken to make sure it will be fixed.

****Duration****: January 25, 2024, 08:00 - 20:00 (EAT)

****Impact****: Outage on an isolated Ubuntu 20.04 container running Apache server. GET requests resulted in 500 Internal Server Errors instead of the expected HTML file, affecting all users during the 12-hour outage.

****Root Cause****: A misconfiguration in the Apache server settings leading to incorrect handling of Python scripts.


****Root Cause and Resolution:****

****Root Cause:**** Misconfiguration in Apache server settings resulted in the incorrect handling of Python scripts, leading to 500 Internal Server Errors.

****Resolution:**** Adjusted Apache server settings to ensure proper handling of Python scripts, allowing for the correct generation of the expected HTML file.


****Corrective and Preventative Measures:****

****Configuration Audits:**** Conduct regular audits of server configurations, especially during new releases, to identify and rectify misconfigurations promptly.

****Automated Testing:**** Implement automated testing scripts to validate server configurations and application functionality after updates or releases.


_In conclusion, this outage highlighted the critical importance of meticulous configuration management and continuous monitoring. The implemented measures are designed to fortify the system against similar misconfigurations, ensuring a seamless user experience during future releases._
