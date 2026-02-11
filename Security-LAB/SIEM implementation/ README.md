## Security Information Event Management ( SIEM ) implementation | Wazuh + Sysmon
### Objective 
The goal of this project is to design and implement a functional SIEM-based monitoring environment using Wazuh and Sysmon to gain hands-on experience in real-world detection engineering and log analysis.

<p>This implementation focuses on:</p>
<ul>
  <li>- Deploying and configuring Wazuh as a centralized SIEM platform</li>
  <li>- Integrating Sysmon for advanced Windows endpoint telemetry</li>
  <li>- Creating meaningful detection rules based on real attack techniques</li>
  <li>- Practicing alert triage and incident investigation workflows</li>
  <li>- Understanding log correlation and event enrichment</li>
</ul>
The objective was not just to build a lab, but to simulate a practical blue team environment where security monitoring, detection tuning, and threat analysis are performed daily.
<p>Officila information about Wazuh you can find <a href="https://github.com/wazuh/wazuh"> on GitHub </a> or <a href="https://wazuh.com/"> on Website</a></p>

### Walkthrough 
<ul>
  <li><b>STEP 1.</b> For my server i used Raspberry Pi ( 4cpu, 8gb, 60gb SD) wth "Ubuntu Server" on it. </li></br>
  <li><b>STEP 2.</b> Configured SSH for access to the my Respberry server and installed Wazuh server,indexer and dashboard on it.
    <img width="1280" height="686" alt="image" src="https://github.com/user-attachments/assets/15212a92-9635-4795-8b84-907b9d8ea484" />
  </li> 
  </br>
  <li>
    <b>STEP 3.</b> Added agents to my Windows & MacOs hosts
    <img width="1280" height="400" alt="image" src="https://github.com/user-attachments/assets/472fa8ab-6ae7-42cb-9927-388b101e212f" />
  </li>
  <li>
    <b>STEP 4.</b>
    Adding Sysmon on both Windows hosts for more detailed logs from Windows Event viewer. 
    <img width="1159" height="881" alt="VirtualBox_Win10-SandboxHost_05_02_2026_20_52_16" src="https://github.com/user-attachments/assets/f3b5b96a-7840-48cc-8333-72e1413f25c0" />
    <p>Successfully  checked that all working</p>
    <img width="918" height="361" alt="image" src="https://github.com/user-attachments/assets/3c155ae5-10d7-4aad-94a5-b9a687790765" />
  </li>
</ul>

### Conclusion
