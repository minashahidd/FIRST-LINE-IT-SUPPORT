#### **NETWORKING FUNDAMENTALS**



###### **Ping Command**

\- Tests connectivity to a host or IP.

\- Use `ping \[host] -n 3` to limit to 3 packets.

\- Output interpretations:

&nbsp; - "Reply from \[IP]" → successful, latency in ms.

&nbsp; - "Request timed out" → no response; possible firewall, host down, or network failure.

&nbsp; - "Host unreachable" → no route exists; local PC cannot reach host.

\- Practical use:

&nbsp; - Verify internet or internal network access.

&nbsp; - Quickly isolate network issues before escalating.



###### **Tracert Command**

\- Traces the path packets take to a host.

\- Use `tracert \[host]`.

\- Output shows each hop (routers, gateway, ISP).

\- Observations:

&nbsp; - "Request timed out" may appear due to firewall; not always an error.

&nbsp; - High latency on a hop can indicate a slow network segment.

\- Practical use:

&nbsp; - Identify where packets fail to reach destination.

&nbsp; - Troubleshoot connectivity issues beyond local network.



###### **IP Configuration**

\- Command: `ipconfig /all` → shows IP, subnet, default gateway, DNS.

\- Use to confirm correct network settings.

\- Practical troubleshooting:

&nbsp; - Incorrect IP → cannot reach network.

&nbsp; - DNS misconfiguration → internet names don’t resolve.



###### **Network Adapter**

\- Disabling and re-enabling adapter resolves many connectivity issues.

\- Test connectivity before and after changes.

\- Document results with screenshots.

\- Practical use:

&nbsp; - Common first-line fix for disconnected users.

&nbsp; - Simulate real-life user troubleshooting.





#### **ACTIVE DIRECTORY BASICS**



###### **Purpose**

\- Centralized management of users, groups, computers, and policies in a domain.

\- Essential for enterprise IT environments.



###### **Key Concepts**

\- Domain → logical network boundary.

\- Domain Controller (DC) → server managing AD services.

\- Organizational Units (OUs) → containers for users/computers.

\- Users → individual accounts.

\- Groups → control resource access.

\- Permissions → assigned via groups or direct rights.

\- GPOs (Group Policy Objects) → enforce policies across users/computers.



###### **Practical Notes**

\- First-line IT typically verifies accounts and permissions.

\- Issues often stem from incorrect group membership or disabled accounts.

\- Do not perform high-level AD changes without Domain Admin rights.

\- Always test access as non-admin user before escalating.



###### **Common Tasks**

\- Check if user account exists and is enabled.

\- Verify group membership.

\- Reset password if required.

\- Document findings for escalation.

\- Check OU placement if folder/resource access is affected.



###### **Commands / Shortcuts**

\- `Win + R → dsa.msc` → opens Active Directory Users and Computers (requires RSAT).

\- `Shift + Right-Click → Run as different user` → test access.

**- `lusrmgr.msc` → local accounts if AD unavailable.**



###### **Troubleshooting Workflow (AD-related)**

1\. Identify issue (user cannot access resource).

2\. Verify user exists in AD.

3\. Check account status (enabled, password expired).

4\. Check group membership.

5\. Test access.

6\. Document and escalate if needed.





#### **PERMISSIONS \& ACCESS THINKING**



###### **Permission Types**

\- Read → view files/folders.

\- Write → create files.

\- Modify → edit/delete files.

\- Full Control → all above + change permissions.



###### **Explicit vs Inherited**

\- Explicit → assigned directly.

\- Inherited → comes from parent folder.



###### **Troubleshooting Workflow**

1\. Identify issue (e.g., "access denied").

2\. Verify account status and group membership.

3\. Check folder/file permissions.

4\. Adjust permissions safely.

5\. Test access as affected user.

6\. Document findings and screenshots.

7\. Escalate if beyond first-line capabilities.



###### **Practical Notes**

\- Access denied often caused by missing group membership, not just permissions.

\- Always replicate issue with a test account.

\- Take screenshots for documentation.

\- Apply principle of least privilege when adjusting permissions.





#### **CORE IT TOOLS**



###### **Task Manager**

\- Shortcut: Ctrl + Shift + Esc

\- Tabs:

&nbsp; - Processes → CPU, memory per app.

&nbsp; - Performance → system overview.

&nbsp; - Users → logged-in accounts.

**- Observations:**

&nbsp; - High CPU/memory → can cause slow PC.

&nbsp; - Terminate non-critical processes safely.



###### **Services.msc**

\- Start, stop, or restart Windows services.

\- Key examples:

&nbsp; - Print Spooler → printing issues.

&nbsp; - Windows Update → update failures.

&nbsp; - DHCP Client → network IP assignment.

**- Notes:**

&nbsp; - Check dependencies before stopping services.

&nbsp; - Verify service status to confirm system health.



###### **Event Viewer**

\- Logs: System, Application, Security.

\- Observations:

&nbsp; - Correlate errors/warnings with user reports.

&nbsp; - Timestamps help identify incident timing.

\- Practical use:

&nbsp; - Provide evidence for escalation if needed.



###### **File Explorer Security**

\- View folder permissions via Security tab.

\- Check effective permissions for users/groups.

\- Document and adjust safely when troubleshooting access.





#### **FIRST-LINE TROUBLESHOOTING WORKFLOW (COMBINED)**



1\. Identify problem from user report or system alert.

2\. Verify account status and system configuration (local or AD).

3\. Check network connectivity (ping, tracert, ipconfig).

4\. Review folder/file permissions and group membership.

5\. Monitor processes, services, and logs (Task Manager, Services, Event Viewer).

6\. Test resolution (log in as affected user or use test account).

7\. Document steps, observations, and screenshots.

8\. Escalate if issue cannot be resolved safely.





##### **PRO TIPS \& REAL-LIFE OBSERVATIONS**



* Always replicate user issues with a test account.
* Use limited ping packets (`-n 3`) to avoid infinite loops.
* Know difference: "Request timed out" vs "Host unreachable".
* Test folder access as non-admin account to confirm permission issues.
* Disable/re-enable network adapters or services to simulate troubleshooting.
* `Shift + Right-Click → Run as different user` essential for testing.
* Task Manager + Event Viewer together identify system vs application issues.
* Document every step with screenshots for GitHub or escalation.
* Follow structured workflow consistently: identify → verify → troubleshoot → test → document → escalate.



