# Honeynet and SOC in Azure


<p align="center">
<img src="https://www.socinvestigation.com/wp-content/uploads/2022/04/Azure-Sentinel-SIEM-Architecture.jpg"height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p></p>
<h1>Working through Alerts in Sentinel</h1>
Here we will work through an example of alerts generated in Sentinel. We will observe and set the ownership, severity, and status of the alert. Then investigate to determine the legitimacy of the alert. 

<h2>Environments and Technologies Used</h2>

- Azure
- Microsoft Sentinel
- KQL



<h2>Set the alert ownership, severity, and status </h2>

<br />


<p>
1. Start by navigating to the Incidents page in Sentinel. Here, we can see Alerts triggered by the rules we set for certain network activities. 
</p>

![1  In Sentinel, Incidents, order by severity](https://github.com/user-attachments/assets/13113d20-75b3-4d41-bd4b-bd69d5bc67f9)

<br />

<p>
2. Select the Alert you want. Here we will look at a successful brute force attempt in Azure Active Directory (Entra ID). This alert is generated when the same entity fails several log-on attempts, then successfully logs on. We can already see some basic information about this Incident: the number of events and alerts, the time created and last updated, and the IP address and username associated with the alert.
</p>

![4  Owner assigned see info](https://github.com/user-attachments/assets/e4c045d1-cd46-4059-a87c-caac651f73d2)


<p>
 3. Set the 3 criteria by selecting each respective section at the top of the Alert details window. Then select the "View Full Details" tab at the bottom. 
</p>

![5  Set Status to active](https://github.com/user-attachments/assets/c56f0890-e6f5-4d6e-8a65-9d69e58f9719)

<h2>Investigate the Alert </h2>

<p>   
4. Here we see more details about the incident, and we can further investigate.  
</p>

![8  Full details page, Activty Log](https://github.com/user-attachments/assets/3fdc1b69-246e-4c3f-94fc-6f95578732bd)

<p>
5. If we select the Entities option, we can see specific information about the IP address associated with the activity. We can also see which log this Alert is generated from.

![10  observe Entities associted, Investigate](https://github.com/user-attachments/assets/2b6bd8fc-b83d-486c-95dc-33bdec3395ee)


<p>
6. Next, we will copy the query rule for this alert and use Log Analytics Workspace to investigate further.

![2  Get query for alert](https://github.com/user-attachments/assets/2e32fbdd-bdb2-4b2d-bf50-00b34c0795c2)



<p>
7. We can break down the large query rule into more specific queries to better understand the cause and nature of the Alert. 

![4  narrowed query to usernameid](https://github.com/user-attachments/assets/bcd6ef3c-3984-4916-aa5a-23eee14c2e41)


<p>
8. With this query, we can see that the IP address observed in Sentinel is the only one associated with a successful Brute Force attempt. This IP address is for a known computer on the network, and these alerts were generated intentionally. 

![5  Where IP was successful](https://github.com/user-attachments/assets/5854445f-b51c-446c-82ba-038eb6163921)

<h2>Close out the alert</h2>

<p>
9. Having discovered the cause of the alert and verified the entities involved, we can close out the alert. 
 
 - Return to the Incident page in Sentinel and select the alert. 

 - Change the status to closed and enter any appropriate notes. We will classify this alert as "Benign Positive-suspicious but expected."
 
 While a successful logon after several failed logons from the same entity is cause for some alarm, we determined the activity was intentional, came from a trusted source, and was not malicious in nature.

![8  Paste notes in comments](https://github.com/user-attachments/assets/4fd70268-d9e3-4d96-8afe-11f906744f2f)




[Click here to return to my Github Homepage](https://github.com/BryanEAtherton)

<br />

