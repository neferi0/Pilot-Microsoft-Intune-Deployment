<p align="center">
<img src="https://garvis.ca/wp-content/uploads/2023/03/image_thumb-1.png?w=244&h=206"/>
</p>

<h1> Pilot Microsoft Intune Deployment</h1>
This is a walkthrough on how I utilized Microsoft Intune to configure and manage a Windows Device deployment.<br/>


<h2> Software & Technologies Used</h2>

- ProxMox (Virtual Machines)
- Microsoft Intune (Microsoft 365 Business)

<h2>Steps</h2>
<h3 align="center">Introduction</h3>
<br />
<p>
<h3 align="center">To preface this project, I lay out the what and why for this project. I have completed the Microsoft Intune course through Microsoft Learn and now want to bolster that knowledge through actual experience to further my skillset. For my project, I will use Microsoft Intune and configure it so that I can manage a Windows device from enrollment through compliance and application deployment. I will use a trial tenant, enroll a Windows 11 device into Intune, create device groups, create compliance, configuration, update, and security policies, deploy applications, and create conditional access policies. I will then test and tweak any settings that may need to be done. With this lab, I’m striving to simulate a real company’s device management environment, which can provide me with hands-on experience with core concepts.  
</p>
<p>
<br />
<h3 align="center">To formally begin, I created a tenant trial through Microsoft 365 Business, which I decided was the best option due to not only gaining access to Microsoft Intune, but you also gain access to an entire suite of applications which can then be used for deployment in Intune (See Figure 1). I then created 3 different test accounts (See Figure 2).
<br />
</p>
<p>
    <img src="https://imgur.com/a/35TbYwK" height="65%" width="75%" />
</p>
<br />
</p>
<p>
    <img src="https://imgur.com/a/vPkb8iB" height="65%" width="75%" />
</p>
<br />
<p>
<h3 align="center">Next, I will create the VM through my ProxMox server. The specs for the VM is that it is running Windows 11 Pro, with 2 CPUs, 8GB RAM, and an 80GB disk. I then verified that it can reach the internet, the device is updated, and that Microsoft services are reachable (See Figure 3).
<p>
<br />
   <img src="https://i.imgur.com/UnzYDYf.png" height="65%" width="75%" />
</p>
<br />
<br />
<h3 align="center">For the next step, I set up free alerts within the budget section of the Billing and Cost Management section of the Azure services (See Figure 4).
<br />
<be />
<p>
  <img src="https://i.imgur.com/TQ86fG3.png" height="65%" width="75%" />
</p>
<br />
<h3 align="center">Setting User and Group with Best Practices </h3>
<br />
<h3 align="center"> In this breakpoint, we set up the group and user as part of best practices, since it is best to not operate the server as the root. For Azure, the IAM has its own website due to has large and expensive that it is, and we create a group for the upcoming lab as well as a user that is tied to my university email address (See Figure 5 and 6).
</h3>
<p>
  <img src="https://i.imgur.com/jHnt4eB.png" height="65%" width="75%" />
</p>
<br/>
<p>
    <img src="https://i.imgur.com/PjB5AiC.png" height="65%" width="75%" />
</p>
<br />
<h3 align="center"> I then set it to where the user must use the authenticator app for the form of authentication (See Figure 7).
<p>
<br />
    <img src="https://i.imgur.com/p0nlIIY.png" height="65%" width="75%" />
</p>
<br />
<h3 align="center"> The next and most difficult part of the breakpoint was to create a role and permission assignment for the user so that they only had access to the create and deploy instances. This was difficult because of the two areas where roles can be assigned, however in the IAM resource group section, I was able to create the role and demonstrate that from the test dashboard (See Figure 8).
</h3>
<p>
    <img src="https://i.imgur.com/VXCmMVZ.png" height="65%" width="75%" />
</p>
<br />
<h3 align="center">Deploying the Azure Virtual Machine</h3>
<h3 align="center"> In this breakpoint, I deployed the Azure VM, which there were some issues because compared to AWS, there are many more permissions that need to be allowed for the user to create and deploy the VM as well as the SSH private key that is needed. Another difference that exists is that the storage type is a minimum of 30 GB and as stated, SSH is allowed from any group rather than restricted to an established security group (See Figure 9).
</h3>
<p>
    <img src="https://i.imgur.com/wys1iaa.png" height="65%" width="75%" />
</p>
<br />
<br />
<h3 align="center">The IPv4 address has also been noted and alerts set to ensure that I do not incur any additional compute costs (See Figure 10).
<br />
<p>
    <img src="https://i.imgur.com/6L9j73b.png" height="65%" width="75%" />
</p>
<h3 align="center">SSHing to Cloud Server</h3>
<h3 align="center">For the last breakpoint, I SSHed into my cloud server by using the “Connect” feature and selecting the option to connect from the Native Host, being my host computer. It then prompted for the private SSH key that was saved to the desktop from the previous breakpoint where it generated a command that I could run in Command Prompt that would correctly SSH into the VM. From the official guide on SSH to Linux from native host, Microsoft reminds to not accept the handshake at first without verifying where the handshake is coming from on the native machine because it can lead to vulnerabilities to man-in-the-middle attacks, so after running the command to know where the handshake was, I accepted the handshake was inside of the machine (See Figure 11).
</h3>
<br />
<br />
<p>
    <img src="https://i.imgur.com/K28QN4P.png" height="65%" width="75%" />
</p>
<br />
<h3 align="center"> I then tested the functionality of the server and made sure that the machine I had all of the vital information for the upcoming lab, such as the private IP address, which I notated was 10.0.0.4 (See Figure 12).
</h3>
<br />
<p>
   <img src="https://i.imgur.com/seAnd8u.png" height="65%" width="75%" />
</p>
<br />
<br />
<h3 align="center"> This concludes the first half of the project.</h3>
