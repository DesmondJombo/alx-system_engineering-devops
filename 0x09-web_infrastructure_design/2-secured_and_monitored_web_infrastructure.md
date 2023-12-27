- Firewalls:  
Reason -Added to control traffic and enhance security by restricting unauthorized access. 
Purpose- Firewalls control traffic flow, preventing unauthorized access and protecting against security threats.
- SSL Certificate
Reason: Ensures encrypted communication between clients and servers, preventing data interception and tampering during transit.
- Monitoring Clients: 
Reason: Used to track the health and performance of the servers and applications, enabling proactive issue identification and resolution.

Why HTTPS:
- HTTPS encrypts data during transmission, safeguarding user information, passwords, and sensitive data from eavesdropping and tampering.

Why Monitoring:
- Monitoring ensures the health and performance of the infrastructure. It helps detect issues, optimize resources, and enhance security.

How Monitoring Collects Data:
- Monitoring clients collect data on resource utilization, error rates, and security events. They transmit this data to a centralized monitoring service like Sumo Logic.

Monitoring Web Server QPS:
- To monitor web server QPS (Queries per Second), configure monitoring tools to track request rates and server response times. Use metrics like Nginx logs and server performance data.

Issues with the Infrastructure:
1. SSL Termination at Load Balancer Level:
   - Issue: SSL termination at the load balancer exposes decrypted traffic within the internal network, reducing security.
   - Solution: Implement end-to-end encryption by encrypting traffic between the load balancer and servers.

2. Single MySQL Server for Writes:
   - Issue: A single point of failure for write operations on the MySQL server.
   - Solution: Implement MySQL replication with a Primary-Replica cluster to ensure high availability and fault tolerance.

3. Identical Server Components:
   - Issue: Uniform components pose a risk; a vulnerability affecting one server may affect all.
   - Solution: Diversify technologies, apply patches consistently, and use security best practices to reduce the impact of potential vulnerabilities.

