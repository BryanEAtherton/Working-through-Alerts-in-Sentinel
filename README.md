# Honeynet and SOC in Azure


<p align="center">
<img src="https://i.imgur.com/Yjq38L7.jpeg"/>
</p>

<h1>Working through Alerts in Sentinel</h1>
Here we will work through examples of Alerts generated in Sentinel. We will observe and set ownership, severity and staus of the alert, then investigate to determine the lagitimacy of the alert. 

<h2>Environments and Technologies Used</h2>

- Azure
- Microsoft Sentinel
- KQL



<h2>Set alert ownership, severity, and status </h2>

<br />


<p>
1. Start by navigating to the Incidents page in Sentinel. Here, we can see Alerts triggered by the rules we set for certain network activities. 
</p>

![1  In Sentinel, Incidents, order by severity](https://github.com/user-attachments/assets/13113d20-75b3-4d41-bd4b-bd69d5bc67f9)

<br />

<p>
2. Select the Alert you want. Here we will look at a successful brute force attempt in Azure Active Directory (Entra ID).
</p>

![2  Select Alert ](https://github.com/user-attachments/assets/bfb423fc-9826-4c65-bd10-899ec38ecb4d)


<p>
 3. Open Windows Event Viewer
</p>
<p>
<img src="https://i.imgur.com/y72gJDw.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>

<p>   
4. Under Windows Logs, Select Application.
<p>
<img src="https://i.imgur.com/WJjbw1j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
5. Here we can see our failed logon attempts and more details about these events in the bottom portion of the window.
<p>
<img src="https://i.imgur.com/F7e5bMk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

[Click here to return to my Github Homepage](https://github.com/BryanEAtherton)

<br />

