#### **Windows User Issues**



##### **Learning Objectives:**

1. Understand the different Windows user account types (Administrator vs Standard) and permissions, including when to escalate vs fix yourself.
2. Diagnose common PC performance issues, including CPU, RAM, disk, and startup problems.
3. Navigate Task Manager, Device Manager, and Services.msc confidently.
4. Use Event Viewer to identify and document system and application errors.
5. Write professional tickets with clear steps taken, actions, and resolutions.
6. Speak confidently to users and managers, using proper IT terminology.
7. Understand real-life IT support environments: prioritizing user impact, escalating critical issues, documenting evidence, and maintaining professional communication.



##### **Core Knowledge:**



###### **Windows User Accounts:**

* Administrators can make system-wide changes, install software, and manage users. Standard users have limited access and cannot change critical system settings.
* **In corporate environments, most users will be Standard users. Admin accounts are only used when required to install software or troubleshoot major issues.**



###### **Task Manager:**

* Shortcut: Ctrl + Shift + Esc
* Use to monitor CPU, RAM, Disk, Network usage. Check which processes use the most resources.
* **Checking Task Manager is often the first step when a user reports a slow PC. Identifying and disabling unnecessary startup apps or heavy processes can solve the problem quickly.**



###### **Device Manager:**

* Shortcut: Win + X → Device Manager
* Use to check hardware, update drivers, disable/re-enable devices.
* **Common first-line issues include network adapters, audio devices, and printers. Knowing how to quickly troubleshoot or restart devices saves time.**



###### **Services:**

* Shortcut: Win + R → services.msc
* Services are background processes required for applications or Windows features to function.
* Common services: Print Spooler (printing), Windows Audio (sound), DHCP Client (network connectivity), Windows Update (system updates).
* Startup types: Automatic (starts at boot), Manual (starts when needed), Disabled (won’t start).
* Dependencies: Stopping one service may impact others. Always check Dependencies tab before stopping critical services.



###### **Event Viewer:**

* Shortcut: Win + R → eventvwr.msc
* Logs: Application (apps crashing), System (hardware/system errors), Security (login attempts).
* **Use Event Viewer to investigate issues, export logs as .evtx, and attach to tickets. This is standard practice in corporate IT support.**
