## SSH Brute Force Detection Scenario
### MITRE | ATT&CK
### Tactic: <a href="https://attack.mitre.org/tactics/TA0006/"> Credential Access </a> 
### Technique: <a href="https://attack.mitre.org/techniques/T1110/"> T1110 | Brute Force </a>
<hr>

### Scenario objective:
Brute force is a credential access technique where an attacker repeatedly attempts authentication using known usernames and multiple password guesses.

### Scenario:
<p>In this scenario, it was assumed that:</p>
<ul>
  <li>A valid username was already enumerated</li>
  <li>The password was unknown</li>
  <li>SSH password authentication was enabled intentionally for testing purposes</li>
</ul>
<p>This environment was configured specifically for detection validation.</p>

### Walkthrough
<p>STEP 1 | Attack Simulation </p>
<p><b>Tool used:</b> Hydra </p>
<p>Steps performed:</p>
<ul>
  <li>Created a simple password wordlist ( used 5 rows for simple test) </li>
  <li>Executed SSH brute-force attack against target server</li>
</ul>

```
hydra -l <valid_user> -P passwords.txt ssh://<target_ip>
```
![photo_2026-02-06_17-26-01](https://github.com/user-attachments/assets/1dc91e19-8f4b-471e-90bd-fc9de4a31485)

### Observed Pattern

Wazuh generated alerts for:
<ul>
  <li>Multiple FAILED SSH login attempts</li>
  <li>Followed by a SUCCESSFUL authentication</li>
</ul>
<p>This pattern is a strong behavioral indicator of a brute-force attack.</p>

<b>Detection Logic</b>
<ul>
  <li>Threshold-based detection (multiple failures in short time window)</li>
  <li>Correlation between failed and accepted authentication events</li>
  <li>Mapped automatically to MITRE ATT&CK T1110</li>
</ul>





