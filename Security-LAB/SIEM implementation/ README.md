## Security Information Event Management ( SIEM ) implementation | Wazuh + Sysmon
### Objective 
The goal of this project is to design and implement a functional SIEM-based monitoring environment using Wazuh and Sysmon to gain hands-on experience in real-world detection engineering and log analysis.

<p>This implementation focuses on:</p>
<ul>
  <li> Deploying and configuring Wazuh as a centralized SIEM platform</li>
  <li> Integrating Sysmon for advanced Windows endpoint telemetry</li>
  <li> Creating meaningful detection rules based on real attack techniques</li>
  <li> Practicing alert triage and incident investigation workflows</li>
  <li> Understanding log correlation and event enrichment</li>
</ul>
<p>The objective was not just to build a lab, but to simulate a practical blue team environment where security monitoring, detection tuning, and threat analysis are performed daily.</p>

<p>Officila information about Wazuh you can find <a href="https://github.com/wazuh/wazuh"> on GitHub </a> or <a href="https://wazuh.com/"> on Website</a></p>

### Walkthrough 
<b>STEP 1 | Infrastructure Setup </b>
<p>For the SIEM server I used a Raspberry Pi 4 (4 CPU cores, 8GB RAM, 60GB SD card) running Ubuntu Server.The goal was to build a lightweight but fully functional SIEM environment that can operate 24/7 in a home lab setup with minimal power consumption.</p>

<b>STEP 2 | Wazuh Deployment </b>
<p>Configured SSH for secure remote access and deployed:</p>
<ul>
  <li>Wazuh Manager (server)</li>
  <li>Wazuh Indexer</li>
  <li>Wazuh Dashboard</li>
</ul>
<br>
<img width="1280" height="686" alt="image" src="https://github.com/user-attachments/assets/15212a92-9635-4795-8b84-907b9d8ea484" />
<br>
<p><b>STEP 3 | Agent Deployment </b></p>
<p>Installed Wazuh agents on:</p>
<ul>
  <li>Windows hosts</li>
  <li>MacOs</li>
</ul>
<p>Verified agent registration and connectivity to ensure log forwarding to the SIEM server.</p>
<br>
<img width="1280" height="400" alt="image" src="https://github.com/user-attachments/assets/472fa8ab-6ae7-42cb-9927-388b101e212f" />
<br>
<p><b>STEP 4 | Sysmon Integration (Windows Telemetry Enhancement)</b></p>
<p>Installed Sysmon on Windows hosts to enhance endpoint visibility beyond default Windows Event Viewer </p>
<p>Sysmon provides:</p>
<ul>
  <li>Process creation events</li>
  <li>Network connections</li>
  <li>File creation/modification</li>
  <li>Registry modifications</li>
  <li>Driver loads</li>
</ul>
<br>
<img width="1159" height="881" alt="VirtualBox_Win10-SandboxHost_05_02_2026_20_52_16" src="https://github.com/user-attachments/assets/f3b5b96a-7840-48cc-8333-72e1413f25c0" />
<br>
<p>After installation, confirmed:</p>
<ul>
  <li>Sysmon operational logs were generated</li>
  <li>Events were forwarded via Wazuh agent</li>
  <li>Telemetry appeared correctly in Wazuh dashboard</li>
</ul>
<br>
<img width="918" height="361" alt="image" src="https://github.com/user-attachments/assets/3c155ae5-10d7-4aad-94a5-b9a687790765" />
<br>
### Conclusion
<p>This project provided practical experience in deploying and operating a SIEM environment with endpoint-level visibility.
</p>
<p>The lab environment now serves as an ongoing security testing ground where I continuously simulate attacks, analyze telemetry, and improve detection capabilities.
</p>
