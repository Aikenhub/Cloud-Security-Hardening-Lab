# Cloud Security Hardening & Audit Lab
**Practitioner:** Anselm
**Focus:** Azure Security & ISC2 Cybersecurity Principles

## 🛡️ Step 1: Network Perimeter Defense
I configured an **Azure Network Security Group (NSG)** to act as a firewall. 
* **Action:** I restricted SSH access (Port 22) to only my administrative IP.
* **Logic:** This follows the **Principle of Least Privilege** by blocking the public internet from attacking the server.
![Network Security](nsg-setup.png)

## 🔑 Step 2: Identity & Access Control (RBAC)
I implemented **Role-Based Access Control** for a user named "Officer_Jane".
* **Action:** Assigned the 'Reader' role.
* **Logic:** This ensures **Separation of Duties**. She can view the system but cannot change security settings.
![IAM Settings](rbac-setup.png)

## 🔒 Step 3: Host Hardening (File Security)
Inside the Linux terminal, I secured sensitive system logs.
* **Action:** Used `chmod 600` on the security log file.
* **Logic:** This protects **Confidentiality**. Even other users on the system cannot read these private logs.
![Terminal Security](chmod-setup.png)

## 📝 Step 4: Security Auditing
I enabled the `auditd` service to track system events.
* **Action:** Created a "Watch" on the password file.
* **Logic:** This ensures **Accountability**. Every attempt to touch sensitive data is recorded for the boss to see.
![Audit Logs](audit-log.png)
