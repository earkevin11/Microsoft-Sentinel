# Microsoft-Sentinel

# What is Microsoft Sentinel?
- It's Azure's SEIM (Security Information Event Management) and SOAR (Security Orchestration Automated Response).
- Solution collects your data across all users, devices, and application 
- It detects undetected threats and hunts for suspsicious activities
- Also can respond to incidents rapdily


# Microsoft Sentinel - Creating a LAW
- Sentinel works on data that gets collected.
- It needs a Log Analytics workspace (LAW)
- Data may take hours to load.

# Add Sentinel to a workspace

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/177023208-6c800d82-4bcb-40c9-9193-fa334100d72e.png" height="65%" width="65%" alt="Resource Locks"/>

<p/>

# Microsoft Sentinel - Azure Activity(Monitor) Connector connection 
- Via the data connectors, users can start collecting data.
- Go to Data Connectors and you can see there are about 122+ connectors.
- You can collect data from other SaaS platforms and Azure-based services.
- We want the data from Azure Monitor to be streamed onto Sentinel.
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/177023277-ef7c42b3-3fc2-432c-b5f3-afd84f8e378d.png" height="65%" width="65%" alt="Resource Locks"/>

<p/>

# Search for Azure Acitivity connector on Sentinel.
- Open Connector Page > Launch Azure Policy Assignment Wizard
- In Scope - select the tenant group that contains all your subscriptions
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/177023315-d8acb1a8-769a-4ad4-97ac-894cce39f003.png" height="65%" width="65%" alt="Resource Locks"/>

<p/>



- Select the LAW workspace you want the data to stream from and CREATE
- From the activity connector, select the LAW workspace created
- Ensure that there are activities in place so you could perform some admin activities so LAW can record it.
- It make take 30 minutes to load up on Sentinel.
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/177023222-cdad05c2-ccd3-4bec-9186-0750a8ec5909.png" height="65%" width="65%" alt="Resource Locks"/>

<p/>

# Data streaned from Azure Monitor to LAW
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/177050373-4ded8c51-a688-461a-a789-134c271820ae.png" height="155%" width="155%" alt="Resource Locks"/>

<p/>




# Microsoft Sentinel - Azure AD Connector
- Goal is to stream data from our Sign-in and Audit logs to a LAW.

# Go to your LAW created and connect Azure AD Connector
- Select Sign-in and Audit logs and apply changes
- Ensure to create some new users or groups, delete groups or users so that the LAW can collect that and stream into Sentinel.




# Microsoft Sentinel - Windows Event Viewer Connector
- We want to collect Security events from our Windows Logs frmo our demovm virtual machine
- From our LAW, navigate to Virtual Machines, and connect the demovm.

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/177051240-230cde99-f8a5-4a78-8c88-ddebd2804700.png" height="155%" width="155%" alt="Resource Locks"/>

<p/>

# Install the Windows Security Events connector via Sentinel
- Open the connector page 
- Select "Create data collection rule"

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/177051398-d7bc924e-b918-4f0e-acc2-f1fc9cf6b7fe.png" height="155%" width="155%" alt="Resource Locks"/>

<p/>

# Add the demovm machine and select create

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/177051511-bd214c31-27b5-459a-91f4-83f2257d4d17.png" height="155%" width="155%" alt="Resource Locks"/>

<p/>
