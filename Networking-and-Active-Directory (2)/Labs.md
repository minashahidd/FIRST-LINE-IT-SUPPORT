###### **Lab – Network Connectivity**

\- Ping google.com (-n 3).

\- Ping unreachable IP.

\- Tracert google.com.

\- ipconfig /all to view IP, gateway, DNS.

\- Observations:

&nbsp; - Verify network configuration and connectivity.

&nbsp; - Identify host unreachable or timeouts.





###### **Lab - DNS Resolution**

Command: nslookup www.google.com

Observation:

\- IP addresses returned successfully

\- DNS resolving correctly → internet accessible by domain name



Command: nslookup 192.168.1.250 (non-existent host)

Observation:

\- DNS query failed / Host unreachable

\- Confirms no device exists or DNS misconfigured





###### **Lab – Network Adapter Troubleshooting**

Step 1: Disabled Ethernet adapter

Observation: Connection lost, IP removed, ping to gateway failed



Step 2: Re-enabled Ethernet adapter

Observation: IP reassigned via DHCP, connectivity restored, ping successful





###### **Lab – Task Manager, Services, Event Viewer**

\- Open Task Manager: Ctrl + Shift + Esc.

\- Monitor processes, CPU, memory usage.

\- Open Services.msc:

&nbsp; - Check/start/stop key services: Print Spooler, Windows Update.

\- Open Event Viewer:

&nbsp; - Review System, Application, Security logs.

\- Observations:

&nbsp; - Identify high CPU/memory processes.

&nbsp; - Check service status for issues.

&nbsp; - Look for errors/warnings in logs.



###### 

###### **Lab – Reset User Password \& Manage Group Membership (Local)**

Environment: Local Users and Groups on Windows 10 Pro

Actions:

\- Reset password for test account (temporary password set, user must change at next login)

\- Verified group memberships for test account

\- Added test account to additional group for testing

\- Used net user and net localgroup commands for command-line verification





###### **Lab – Permissions \& Access Thinking**

\- Simulate access denied to folder C:\\TestFolder.

\- Verify user account and group membership.

\- Review folder permissions (Read, Write, Modify, Full Control).

\- Adjust permissions safely.

\- Test access with test account.

\- Observations:

&nbsp; - Explicit vs inherited permissions can affect access.

&nbsp; - Always document steps and screenshots.



