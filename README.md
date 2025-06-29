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
2. Select the Alert you want. Here we will look at a successful brute force attempt in Azure Active Directory (Entra ID). We can already see some basic information about this Incident. The number of events and alerts, the time created and last updated, and the IP address and username associated with the alert.
</p>

![4  Owner assigned see info](https://github.com/user-attachments/assets/e4c045d1-cd46-4059-a87c-caac651f73d2)


<p>
 3. Set the 3 criteria by selecting each respective section at the top of the Alert details window. Then select the "View Full Details" tab at the bottom. 
</p>

![5  Set Status to active](https://github.com/user-attachments/assets/c56f0890-e6f5-4d6e-8a65-9d69e58f9719)



<p>   
4. Here we see more details about the incident, and we can further investigate.  
</p>

![8  Full details page, Activty Log](https://github.com/user-attachments/assets/3fdc1b69-246e-4c3f-94fc-6f95578732bd)

<p>
5. If we select the Entities option, we can see specific information about the IP address associated with the activity. We can also see which log this Alert is generated from.

![10  observe Entities associted, Investigate](https://github.com/user-attachments/assets/2b6bd8fc-b83d-486c-95dc-33bdec3395ee)


<p>
5. Here we can see our failed logon attempts and more details about these events in the bottom portion of the window.
<p>
<img src="https://i.imgur.com/F7e5bMk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<p>
5. Here we can see our failed logon attempts and more details about these events in the bottom portion of the window.
<p>
<img src="https://i.imgur.com/F7e5bMk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>



<p>
5. Here we can see our failed logon attempts and more details about these events in the bottom portion of the window.
<p>
<img src="https://i.imgur.com/F7e5bMk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


[Click here to return to my Github Homepage](https://github.com/BryanEAtherton)

<br />

