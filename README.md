<h1>Building a Honeypot Lab with Microsoft Sentinel for Live Attack Monitoring</h1>
<p align="center"><img src="https://i.imgur.com/A9OlwiZ.png" height="80%" width="80%"/></p>

<h2>Description</h2>
I set up a vulnerable virtual machine as a honeypot, exposed it to the internet, and used Azure Log Analytics to track failed login attempts. Then, I analyzed the data in Azure Sentinel and created a heatmap showing the attackers' locations on a world map.<br />


<h2>Tools Used</h2>

- <b>Azure Virtual Machine</b> 
- <b>Microsoft Sentinel</b> 
- <b>Azure Log Analytics Workspace</b> 

<h2>Walk-through:</h2>

<p align="center">
Create a virtual machine with minimal security to attract attackers.<br/>
<img src="https://i.imgur.com/QUmL3su.png" height="80%" width="80%"/>
<br />
<br />
Remove all firewall rules and configurations on the VM to make it more vulnerable to attacks.<br/>
<img src="https://i.imgur.com/XflrMJy.png" height="80%" width="80%"/>
<br />
<br />Link the VM to an Azure Log Analytics Workspace to collect and analyze log data..<br/>
<img src="https://i.imgur.com/N2oXo1P.png" height="80%" width="80%"/>
<br />
<br />
Downloaded and run a custom PowerShell script (from GitHub) that retrieves the geolocation of potential attackers. Execute the script to gather geographic data (e.g., country or city) on any attacker interacting with your VM.<br/>
<img src="https://i.imgur.com/AHyO0Vt.png" height="80%" width="80%"/>
<br />
<br />
Uploaded a custom log format and upload it into the Log Analytics workspace tables, specifying how you want the logs to be structured.<br/>
<img src="https://i.imgur.com/C093bzU.png" height="80%" width="80%"/>
<br />
<br />
Set up a map in Microsoft Sentinel to visualize the geolocations of attackers by country, providing insight into the source of attacks.<br/>
<img src="https://i.imgur.com/A9OlwiZ.png" height="80%" width="80%"/>
<br/>
<br/>
Here's our dashboard overview look.<br/>
<img src="https://i.imgur.com/Ax05E9L.png" height="80%" width="80%"/>
