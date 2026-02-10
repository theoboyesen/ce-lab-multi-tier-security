I have followed 2 core principles whilst designing this security architecture.

- Least privilege (Each tier only has the minimum access it requires in order to function)
- Defense in depth (Security is enforced at multiple layers including: Subnets, Security groups, Bastion access pattern)

Bastion tier 
- Acts as a single SSH entry point into the environment. Placed into a public subnet with a public IP, SSH is only allowed from my personal IP.
This reduces the attack surface and makes access control and auditing simpler as admin access is centralised to one host.

Web tier
- Handles HTTP (80) and HTTPS (443) traffic from the internet. There are no public IPs assigned and SSH is allowed only from the bastion.
This prevents attackers gaining admin access via the public interface.

App tier
- Proccesses requrests from the web tier and talks back to the database. There are no public IPs assigned and SSH is allowed only from the bastion.
This prevents direct internet access to backend services.

Database tier
- Stores data.  There are no public IPs assigned and SSH is allowed only from the bastion. The most restricted component, it is never exposed to the internet 
or the web tier, ensuring sensitive data is highly controlled.

This archiecture implements a desfense in depth security model using tiered security groups and a bastion host access pattern. Public traffic is limited to the web
tier, admin access is centralised through the bastion host, and internal communication is strictly controled using security groups. Each tier is isolated and granted only
the permission it requires.