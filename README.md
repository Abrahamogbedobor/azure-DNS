<p align="center">
<img src="https://i.imgur.com/OYy9qqX.png" alt="Domain Name Server"/>
</p>

<h1>Domain Name Server (DNS) and Network File Permission</h1>
In this tutorial, we observe various ne. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Active Directory running in Azure on a Virtual Machine (DC_1)
- A client machine running in Azure on a virtual machine (Client_1) and joined to the domain

<h2>Operating Systems Used</h2>

- Windows 10 (21H2)
- Window Server 20.04

<h2>High-Level Steps</h2>

- Inspecting DNS A-records on a server (Hostname to IP address mappings)
- Creating new A-records on server (DC_1) and then observe them from the client machine
- Deleting records from server and then inspect/clear client machine DNS cache in order to gain understanding 
- CNAME records (Mapping one hostname to another hostname)
- Root hints

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/QwCQbmt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/HGgHcOY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Fu8RNjh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/P8qDPIJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In order to inspect A-records on a server, both Client_1 and DC_1 computer were remotely connected into as admin and domain admin respectively. Then Client_1 was used to ping a site called 'MAINFRAME'. The result shows no record was found. Figure1 above was used to illustrate how DNS works, and the preceeding figures were used to further explain DNS in details. From the figures abiove, Client_1 tries to ping a site first, it checks its own 'cache' to see if it could get an IP address for mainframe no result second, it check 'host file' available on all windows computer at c:\windows\system32\drivers\etc\hosts also no IP address that matches mainframe hostname. Then lastly, it check its local DNS server DC_1, from the figure above the DNS server cheked and says idk that's when the error message for ping result returns as failed.
</p>
<br />

<p>
<img src="https://i.imgur.com/aLLclBO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/3eE9wSw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This session created A-records on DC_1 server by mapping mainframe to DC_1 IP address
</p>
<br />

<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
It 
</p>
<br />
