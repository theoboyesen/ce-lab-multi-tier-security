There are 2 seperate traffic paths in this system

- User traffic
- Admin traffic

User traffic
- Users access the app over HTTP (80) or HTTPS (443),
this is the only tier exposed to public traffic.
- The web tier forwards requests to the app tier on TCP port 8080,
only the web tier security group is allowed to initiate this traffic.
- The app tier connects to the database on TCP port 3306, this is
the only path allowed to the database.
- All responses flow back through the same path

Admin (SSH) traffic
- SSH access on port 22 is restricted to my personal IP
- The bastion host is the only publicly accessible instance for admin
- The bastion initiates SSH connections to: Web tier, App tier, Database tier
- No internal instance accepts SSH directly from the internet


