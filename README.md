# Task-4
Performed configuration and testing of firewall rules to control network traffic by blocking and allowing specific ports as part of a Cyber Security Internship.

# 🛡️ Task 4: Setup and Use a Firewall

## 📌 Description
Configured and tested firewall rules to control network traffic by blocking and allowing specific ports as part of a Cyber Security Internship.

## 🎯 Objective
To understand how firewall rules filter network traffic by creating, testing, and removing rules for specific ports.

## 🛠️ Tools Used
- Firewall configuration tool (system firewall / terminal-based utility)
- Command line interface
- Network testing tools (nc / telnet)

## ⚙️ Steps Performed
1. Opened firewall configuration tool through system settings or terminal.
2. Listed current firewall rules using:
   sudo pfctl -s rules
3. Opened firewall configuration file using:
   sudo nano /etc/pf.conf
4. Added rule to block inbound traffic on port 23 (Telnet):
   block in proto tcp from any to any port 23
5. Applied firewall changes using:
   sudo pfctl -f /etc/pf.conf
6. Enabled firewall (if required) using:
   sudo pfctl -e
7. Tested the firewall rule using:
   nc -vz localhost 23
   (Expected result: connection failed or timed out)
8. Removed the test rule by editing /etc/pf.conf and reloading firewall:
   sudo pfctl -f /etc/pf.conf

## 📊 Outcome
Successfully configured and tested firewall rules to block inbound traffic on port 23 (Telnet). The rule was verified using network testing tools, and the system was restored to its original state after removal of the rule.

## 📘 Key Learning
- Firewall configuration and management
- Port-based traffic filtering
- Difference between allow and block rules
- Testing network connectivity using terminal tools
- Understanding how firewalls enhance system security
