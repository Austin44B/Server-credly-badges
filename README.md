# Server-credly-badges
Explanations of each badge earned through real world lab environments to test understanding of the Server+ skills outlined by Comptia.

#

    Table Of Contents :
      1) Architecture
      2) Governance, Risk and Compliance
      3) Infrastructure
      4) Networking
      5) Operations
      6) Security
      7) Troubleshooting

      Note : Each badge hyper link is to Credly to verify the earning of the badge, and some additional 
              information.
#

##

<img width="267" alt="image" src="https://github.com/Austin44B/Server-credly-badges/assets/134319619/ec528a81-13a6-46cf-a083-55a81accb691">

In earning the Server+ [Architecture](https://www.credly.com/badges/a4e3a24e-3efe-4562-a907-5eb6e67c5af1/public_url) badge :

Server+ is going to be dense with information, those of you whom wish to entertain me, and read through are welcome to, though fair warning, it's going to be a lot, I thank you for starting here, and wish you the best in your journey through life :) 

Starting off Server+ we have the Architecture badge. A virtual instance can be provisioned as a virtual machine running a complete OS or as a container, running just the code needed to implement an app. Being able to deploy both types of instances will be critical to success in a career as a server administrator.

Modern networks are increasingly cloud-based, The MS10 member server is typical of workgroup or corporate server provisioning, where a single server machine is configured to perform a variety of roles, such as file server, web and email messaging, each role is configured in a dedicated virtual instance. Not only can Virtual machines be used in production, but they are also for development and testing.  It is useful to provision multiple types and versions of operating systems, platforms, and clients to ensure that an app works equally well across all of them, we can achieve this by using Virtual machines on different platforms ( Such as Microsoft's Internet Information Server (IIS) and Apache ) for development and testing before production. While setting up virtual machines on a hypervisor it important to ensure that the VM can communicate with the host but if needed is isolated from the domain network, we can do this by configuring critical performance and security settings for the VM and the hypervisor. During configuration consider how Virtual Switches may play a part in the network as well.
Following up the setting up of virtual machines on hypervisors, we can also deploy and manage docker containers. Deploying applications within a VM running a full OS can be time-consuming. Using Containers we have a faster and more efficient way to build and deploy various types of instances, such as deploying server or desktop operating systems, implementing databases and web apps, deploying networking appliances, and virtually any other computing task. One way to practice learning this skill is using a intentionally vulnerable web app as a Docker container developed by OWASP called "Juice Shop". Make to do this in a controlled environment as the web app being vulnerable can be used to learn other skills as well.

As nice as containers are for rapid easy deployment. To create a stronger knowledge base, knowing how to use manual setup for programs and package managers helps to understand how such tasks can be scripted and automated using tools such as Ansible and Chef for server deployments. A fun project to practice learning this knowledge is deploying a Ubuntu server and installing a Linux, Apache, MySQL, PHP ( LAMP) application stack that is ready for configuration. Debian-based distributions such as Ubuntu use the apt package manager, we use the apt to check for routine updates and even install a Apache server. Apache is one of the top 3 web servers by usage ( the others being nginx and Microsoft's Internet Information Services (IIS) ). After installing a Apache server we would want to configure the firewall so that only incoming web and secure shell (SSH) traffic is accepted. We can also Set up a LAMP server which can run the LInuxOS, Apache web server, MySQL database, and PHP hyperText processor scripting environment ( Acronym being "recursive" ). PHP can also be used to create a script to test connectivity with a MySQL database service. 

Using those Servers we could set up, is a great lead into configuring Administrative Interfaces which allows for remote management by using secure Shell (SSH) to manage the servers over the network and configure secure password-less access to the administrative interface using public key cryptography. While this makes management easier, given the nature of modern security threats, it also exposes the server to greater risk of compromise if the client workstations, tools and protocols used for remote administration are not secured ( hardened ) against compromise. A secure administrative workstation is referred to as a SAW. SAWs should be installed with a minimal amount of desktop software and restricted from general web/email/office document use. Some SSH software  to note is PuTTY which implements a terminal only while WinSCP is primarily a GUI client for managing files using FTP over SSH (SFTP) plus other remote file management protocoles. WinSCP is freeware developed by Martin Přikryl and Putty is written and maintained primarily by Simon Tatham.
When there are tens or hundreds of server to manage, SSH connection can also be authenticated by a client key, which is when a server is configured with public keys of trusted clients instead of using a password. 

Some notes to end with :

• Private keys are kept secret. It must be stored securely on the user's computer or a secure USB key and only accessed by an authorized account.

• The public key identifies the subject (user or computer) as the owner of the linked private key. This public key is copied to the SSH server. Because of the way public key encryption works, the server can trust that the user holds the private key linked to the public key and authenticate them.

To wrap up the Architecture badge, A last piece of useful information that can streamline efficiency as a Administrator, is the ability to configure resilient file servers with failover file server clustering. All those metaphorical VM from containers working hard for us, we wouldn't want to be lost for some unseen event. A cluster provisions a service using multiple nodes. A cluster can be configured to load balance processing effort and/or to provision failover resiliency. Failover means that if one node stopes working, the cluster service continues to operate on the remaining nodes. Advanced clusters can sustain services when multiple nodes fail. When setting up a cluster each node in a cluster must be able to access the same storage resource. The nodes use a state system to determine which are able to write to the storage at any one time to avoid conflicts. Clustering usually works best when all the nodes are as similar as possible, in terms of both hardware platform and OS version, Good thing we learned how to leverage containers to streamline the process of setting up VMs ! Using a cluster management tool assists in the process of validating requirements and configuring nodes, networks, and shared storage. Clusters are often used to provision virtual machines and databases, Configuring a fully resilient service, requires eliminating all single point of failures (SPoF).

Thank you for reading ! 

Best Wishes and Sincerely,

Austin B.

The CompTia Server+ Architecture badge covers exam objectives in sections, 2.1, 2.2, 2.3, 2.4, 2.5

##

<img width="265" alt="image" src="https://github.com/Austin44B/Server-credly-badges/assets/134319619/18d02c2e-daa0-40f8-ba28-73e4c2939232">

In earning the Server+ [Governance, Risk, and Compliance](https://www.credly.com/badges/6319b459-6cdb-44da-ad4e-1d8402bdd392/public_url) badge : 

Within the Governance, Risk and Compliance Badge, we first take a look at Configuring backup solutions on a windows server.
When configuring backups on production networks, consider media storage and rotation schemes. These balance costs (provisioning media capacity and offsite storage) against speed (time to create backups and perform restore operations) and resiliency (a restore point objective, or the amount of data loss that can be tolerated).
Within that overall scheme, we can distinguish two main kinds of backup operation:

 • Data backup makes copies of files and/or database information that changes frequently.

 • System backup make copies of server configurations (OS and applications installed, patched, and configured to a particular baseline). These baseline configuration would not be expected to change so often.

Because of the different requirements, it is often a good idea to perform system and data backups as separate operations.
In addition to backup solutions on Windows, it is important to be well rounded by knowing how to configure backup solutions on Linux as well. Frequent backups prevent catastrophe in a disaster event by having a restore point. Data availability is a key component of security. Mass storage drives fail, data is corrupted or accidentally-deleted, or changed in an unplanned manner. A comprehensive backup plan will account for offsite storage and versioning. We can use NFS share to back up files to a remote server.

Simply put, Save often and make sure that save is secure and ready to deploy in case of disaster. 

Best Wishes and Sincerely,

Austin B.

The CompTia Server+ Governance, Risk, and Compliance badge covers exam objectives in sections, 3.7.

##

<img width="264" alt="image" src="https://github.com/Austin44B/Server-credly-badges/assets/134319619/02eaacf0-9c61-427a-aa17-ffc4328de2e9">


In earning the Server+ [Infrastructure](https://www.credly.com/badges/8fdf0fb5-e222-4c90-a3b8-2f4e79e3a442/public_url) badge : 

Let's begin reflecting on information from the Infrastructure badge, by first looking into managing system inventories. We can use built-in windows and Linux utilities to gather hardware inventory data. Documentation is essential to running efficient and reliable services. A key part of documentation is an accurate and regularly updated inventory of hardware and software assets. Inventory management also involves recording configuration and performance baselines. These baselines can be used to detect configuration drift or reduced performance and are a key reference when troubleshooting issues or obtaining vendor support. Though it is possible to use dedicated inventory management software products to fully or partially automate the process, it will offer the most understanding manually knowing how gather key data using built-in Windows and Linux Utilities. The system information tool (msinfo32) on Windows has historically been the go-to location for hardware and software platform information. We can use the Cockpit web management app and CLI tools to report system hardware information on a Linux host. 

Knowing how to configure RAID storage in Windows is foundational knowledge as Most data assets should be kept on a storage system backed by Redundant Array of Independent Disks (RAID). The risk of catastrophic data loss is too high to use a single disk solution, especially as storage devices are relatively inexpensive to provision. Most enterprise solutions are based on hardware RAID, where the array logic and functionality is located in a dedicated controller device. Software RAID, implemented by the OS, can be cost-effective and is also a useful option in development environments. A hardware RAID solution can use firmware tools to identify each device in an array, while we can use the OS's admin tools to report the information for software RAID. 
There are two basic RAID configurations:

 • Mirroring (RAID 1) means that each file write is duplicated to two disks. If one disk fails, the volume will continue to work. The drawback is that only 50% of the disk space is available.

 • Striping with parity (RAID 5) means that file data is distributed (striped) among a group of disks, along with parity information. The data and parity is distributed so that if one disk fails, it is possible to reconstruct the whole set of data from the information remaining on the functional disks. RAID5 has better storage efficiency (n-1*usuable capacity, where n is the number of drives).

Striping and mirroring have different performance, security, and cost characteristics. They can be combined in nested RAID solutions. For example, RAID10 is a stripe of mirrors, deployed to overcome some of the write performance problems associated with mirroring.

We can also create a RAID block device on a Linux server and configure it as a SCSI target that connects using a Windows server to be a mountable device as a volume. 
A storage area network (SAN) is a high-bandwidth, high-capacity pool of storage devices that can be configured flexibly to meet different application server demands.
A file share protocol such as Samba offers the OS file level access to the share. The disk is formatted by the OS that hosts the share. A SAN is typified by block-level storage. This means that the storage server, referred to as a target, provisions disk resource as block devices. The file/application/database server consuming the storage (referred to as the initiator) can attach one or more of these devices and format them in whatever way is most appropriate.
SANs use the Small Computer System Interface (SCSI) language to communicate input/output commands between the target and initiator. Many SANs implement SCSI within as part of a dedicated storage network physical and data link technology, such as Fibre Channel or Infiniband. iSCSI (Internet SCSI) is a way of deploying a SAN over IP networks.

As briefly touched in the last subject, Linux offers excellent support for configuring software RAID and can be integrated into a Windows domain environment and configured as a file server using the Samba package. Samba implements Windows' Server Message Block file sharing protocol so there is no need for additional client software or protocols. We can create a logical volume using a logical volume manager (LVM) to configure a RAID storage device that is configured as an SMB share. 

Let us finish up the Infrastructure badge with taking a look at managing virtual memory, we can analyze the virtual memory subsystems of windows and Linux hosts. 
The OS kernel exposes physical memory to user-mode processes as a virtual memory device. This allows the OS to protect the memory resource from faulty processes and conflicting demands. The OS uses standard 4K blocks called pages to map virtual memory address space to the physical address space. If demand for memory exceeds the amount of physical RAM installed, the OS can provide more virtual memory address space by writing pages to a different storage medium, such as a disk drive. This destination can be configured as a pagefile stored on a logical volume or as a dedicated partition.
The OS's memory management procedures identify pages that are not being actively used and moves them to the pagefile. A page fault occurs when the OS needs to move a page of memory from the pagefile to RAM. As disk-based storage is often slow, excessive page faults can be a sign that a server does not have sufficient resources to meet demand.
Virtual memory and pagefile usage can be critical factors in server performance. It is important to be able to analyze pagefile activity as computers with hard disk drives (HDDs), the performance gap between the disk subsystem (slow) and the memory subsystem (fast) means that high numbers of page faults can cause numerous problems. Paging increases the number of disk I/O operations, reducing time for other applications to use the disk. This can be mitigated by provisioning dedicated disks for use for paging or by increasing system RAM.

Though this badge was far more exclamational and less exciting as some others I've written, I hope that some information was of potential interest to you, If not, I applaud you for making it this, far. I'm listening to some Chinese music that was turned "epic" and it's quite a epic mood while reading and writing :) 

Have a epic journey through your day today, do something difficult and rise to the occasion, no matter how difficult it is perceived.

Best Wishes and Sincerely,

Austin B.

The CompTia Server+ Infrastructure badge covers exam objectives in sections, 1.2,  2.3, 2.7, 4.3.

##

<img width="263" alt="image" src="https://github.com/Austin44B/Server-credly-badges/assets/134319619/bd0f09d7-c605-45e9-8565-610e0f8afd64">

In earning the Server+ [Networking](https://www.credly.com/badges/e2d6a414-9f75-43de-8680-43ab36629a35/public_url) badge : 

To manage network configurations we can use command-line tools to configure network interface and name resolution on windows and linus hosts. Configuring network settings, needs both a strong understanding of IP addressing concepts, the various utilities and configuration files. It is worth knowing how to configure network adapter properties  using PowerShell in Windows. A understanding of PowerShell is vital as servers are often deployed in server core mode, using scripts to automate the process. Server core mode means there is no desktop interface.

Network Manager is used to configure networking on many modern Linux distributions, replacing the older scripts that read the configuration from /etc/network/interfaces. On desktop versions of Linux, it is designed as a user-friendly graphical means of managing Ethernet, wireless, and VPN connections. On a server, networking can be configured using the nmcli tool.IP addressing is only one part of a working network configuration. Name resolution is also crucial to the functioning of modern networks.
Accurate, up-to-date diagrams and documentation are cornerstones of network management. They need to be updated every time a configuration is changed. Having poor quality documentation will make troubleshooting more difficult and security problems more likely.
There are many factors to consider when creating network diagrams, but two important principles are:

 • Use separate diagrams to represent layer 2 and layer 3 of the OSI troubleshooting model. Mixing too much detail in a single diagram is difficult to interpret and harder to maintain.

 • Tag documentation with contact and date/version information. Other technicians who rely on the documentation need to know who to go to with questions.

At layer 3, we are less concerned about how hosts are connected by adapters and cabling and more about which logical networks they belong to, as defined by their IP address and network prefix or subnet mask. 
Manual configuration of network settings is time-consuming and highly susceptible to errors. For most servers, it is best to use autoconfiguration. The two main tools for doing this are the Dynamic Host Configuration Protocol (DHCP) and Domain Name System (DNS) servers.
Most service-to-service communication and almost all user-facing apps depend on named resources rather than using IP addresses directly. DNS provides a system for sharing records about how host names and domain namespaces map to IP addresses.

Thank you for reading, Have a blessed day,

Best Wishes and Sincerely,

Austin B.

The CompTia Server+ Networking badge covers exam objectives in sections, 2.2, 2.7.

##

<img width="261" alt="image" src="https://github.com/Austin44B/Server-credly-badges/assets/134319619/4410f454-99ef-4a87-8e17-5d65df780b6e">

In earning the Server+ [Operations](https://www.credly.com/badges/91b02a26-536b-4d6a-b654-103fef653213/public_url) badge : 

Starting off the Operations badge I learned about reporting windows server specifications. Servers can be managed using a variety of GUI consoles, web management apps, and command-line utilities.
Being able to navigate these consoles and knowing the usage of command-line tools to implement configurations quickly and accurately is an essential competency.
Server Manager is the principal administration interface for Windows Server with desktop experience. Rather than accessing servers directly, use a management workstation.
Services are the processes that implement whatever role the server instance is deployed for—file sharing, web hosting, email hosting, and so on. 

Following up Windows I then learned about reporting Linux server specifications. 
When selecting a suitable operating system for a project, you must judge between competing requirements, such as cost, stability/support, and innovation. While Windows has only commercial options, Linux is available in many types of distribution with varying levels of cost and support.
Fedora is a free and open-source (FOSS) distribution, but is very closely aligned with the commercial Linux distribution Red Hat Enterprise Linux (RHEL). Where RHEL focuses on platform stability, Fedora is a test bed for new features. Versions are released often and are only supported with updates for a brief period.
Whichever distribution or mix of distributions you select, as with Windows you must keep accurate and up-to-date documentation about all the physical and virtual servers deployed on your networks. The information you will need to collect will be a mix of service tags and model/part numbers, hardware and software inventories, and key facts about the resources—compute, storage, and network—available to each server.
While many Linux admins prefer command line tools, there are plenty of GUI and web management utilities for Linux servers. We can use Cockpit web administration interface to manage a Fedora Server instance for example.

Assessing the topology of a local network and the services that are running on it, and using a firewall to remediate security violations can be described as auditing network services. The sophistication of modern cyber threats mean that no organization can afford to treat security as secondary to functionality. Network designs and server roles must be designed with security as a primary requirement from the outset.

In learning how to monitor performance in Windows, I learned about how a performance monitor measures the utilization of system resources (CPU, memory, storage, and networking). Baseline performance should be measured when a server is deployed into a role or after an upgrade or other change of use. Subsequent monitoring can determine if the server is performing worse than the baseline.
There are many scenarios where there is no opportunity to evaluate "typical" usage. In development environments, monitoring can be conducted using a test suite in the absence of actual usage data.

In conjunction with Windows I learned about monitoring performance in Linux. Linux has many command line and graphical tools that you can use to monitor performance and availability. Availability monitoring detects periods of unexpected downtime and/or periods when performance does not meet agreed standards. This monitoring is critical to meet any contractual obligations set out in service level agreements (SLAs) with internal business units or external customers and partners.

In learning how to analyze configuration baselines I Exported domain controller policy settings and compared them against Microsoft's benchmark using the Security Compliance Toolkit (SCT) Policy Wizard. Policies determine what users can and cannot do in terms of configuring computers on the domain. One aim of policy design is typically to enforce least privilege, so that users have the minimum possible rights to perform their job effectively. However, there are thousands of possible settings to configure across different operating systems, OS versions, and applications software.
Configuring policies incorrectly can have catastrophic security implications. For example, on a Windows network, allowing weak NT password versions, widely exploited versions of SMB, or weak cryptographic ciphers could all allow an attacker to compromise systems with ease.
Vendors assist their customers by creating secure baseline configuration templates. For example, Microsoft provide the Security Compliance Toolkit (SCT) to help administrators evaluate policies against these baselines.

So much to learn, to read, to think about, in the end it is all fascinating, and organizing all my notes to be catalogued here, provides me the opportunity to reflect on my work as time passes :)

Best Wishes and Sincerely,

Austin B.

The CompTia Server+ Operations badge covers exam objectives in sections, 2.2, 2.3, 2.7, 2.8, 3.5.

##

<img width="265" alt="image" src="https://github.com/Austin44B/Server-credly-badges/assets/134319619/ba4bb8d3-2f44-4554-a114-2e25a84ffed0">

In earning the Server+ [Security](https://www.credly.com/badges/68a2846c-8c1b-4d20-b26c-df0f0e3b6920/public_url) badge : 

Successful troubleshooting often depends on the ability to locate information in log files (as well as ensuring that relevant events get logged).
Using log files can be complex, as the OS and applications can write to different files and troubleshooting might encompass events occurring on multiple different servers. There are plenty of Security Information and Event Management (SIEM) products available to assist with aggregating logs from different sources and correlating events to identify causes. These are not always available, however, so you should also be able to perform these tasks using basic tools, such as Event Viewer and powershell cmedlets. The problem with filtering in the Event Log console is that filtered events have no context. To diagnose a problem, you must often examine a sequence of events, some of which may be written to different log files. You can overcome the limitations of Event Viewer by using PowerShell cmdlets to query multiple log sources.

While Windows uses a single event management subsystem, on a Linux server as well as multiple log file destinations, you also need to identify the packages used for logging. Several are available, and more than one might be deployed, depending on the distribution. Like many modern Linux distributions, Fedora uses the Journald logging engine, implemented as part of the systemd startup manager. As this system stores data in binary format, to view journald messages, you must use the journalctl command. 
Rsyslog is a current implementation of the older syslog logging daemon and messaging protocol. Syslog listens to logging sockets on the local machine and (optionally) over the network (on UDP port 514 by default).
The syslog (or rsyslog) conf file determines how those log messages are processed, such as writing to a file, forwarding out over the network, or printing to the terminal. Unlike journald, all syslog messages are processed as plain text.

It is important to audit accounts and permissions in windows. Storage is usually provisioned for the purpose of hosting resources, often either file storage or a database. In both cases you need to ensure that the resources are secured against unauthorized access. This is typically accomplished through access control lists (ACLs). Each resource, such as a file or folder, is tagged with an ACL. The ACL contains entries about which subjects (user and group accounts) have permissions (read, read/write, or full control). When a user requests access, the OS evaluates the user's claims (based on permissions allocated to their account plus permissions obtained via group memberships) and determines the level of access that should be granted.

The scope of a security group determines what permissions it can be allocated and what types of account can be made members of the group:

 • Local groups can be granted permissions on the same computer only. Local groups are stored in the computer's Security Accounts Manager (SAM) registry, not in Active Directory. A local group can contain any type of domain account as a member, however.

 • Domain local groups can be granted permissions on any resource (such as a server's file share) within the same domain. Members of domain local accounts can be of almost any type of 
scope.
Note the distinction between local and domain local groups. A local group has the scope of a single computer only; a domain local group can be assigned permissions on any member of the same domain. It is helpful to think of domain local as meaning "domain resource" to distinguish the two.

 • Global groups can be granted permissions across a forest, but can only contain user/computer and global security accounts from the same domain. Note that a domain local scoped group cannot be a member of a global group.

There are lots of default group accounts you could use, but these tend to have inappropriate privileges (such as the right to log on to the DC). The Delegate Control feature allows an to be granted limited permissions over a subset of network objects that have been assigned to OUs.

When configuring server roles. Application role design must balance performance, security, and resiliency requirements against costs. All three of performance, security, and resiliency can be improved by dedicating separate server hardware to specific roles, but only at increased cost.

One of the most important post-installation tasks is to ensure that security settings meet the requirements of the server role. In a Windows domain environment, this is achieved by configuring group policy objects (GPOs).

As I near the end, I do my best to remind myself not to rush, to enjoy the process, all the time and effort that has been put forth to this project, how much it has reinforced the information I'm learning, and how it expands my ability to have conversation with other whom are in cybersecurity.

Best Wishes and Sincerely,

Austin B.

The CompTia Server+ Security badge covers exam objectives in sections, 1.2, 2.3, 3.5 4.2, 4.4.

##

<img width="273" alt="image" src="https://github.com/Austin44B/Server-credly-badges/assets/134319619/540e25e9-50f5-4ed9-85b3-4a2d70dae26e">

In earning the Server+ [Troubleshooting](https://www.credly.com/badges/2c3f033a-82d0-4581-8aa8-b697313c30bf/public_url) badge : 

To troubleshoot issues effectively, we must approach problems in a structured way. Familiarize ourselves with the steps in the CompTIA troubleshooting model. The first steps are as follows:
	
 • Identify the problem and determine the scope.
	
 • Establish a theory of probable cause (question the obvious).

 • Test the theory to determine the cause.

Another factor in successful troubleshooting is to select appropriate tools and information sources to help to diagnose the problem.When troubleshooting a network problem, a standard approach is to test by OSI layer and work up or down. Investigate applications and services and then proceed to IP connectivity. 
Once we have diagnosed the problem, we then plan and implement a solution:

 • Establish a plan of action to resolve the problem.

 • Implement the solution or escalate.

We do tend to concentrate troubleshooting effort on diagnosis. However, the number of steps in the CompTIA model later in the process emphasize the importance of the structured approach. You can't make unplanned changes to configurations just to solve one problem. Changes must be planned, tested, and approved before they are made.
We can't adjust the MAC address in this lab environment, but in a normal environment, you'd check Device Manager to ensure that both machines are using burned-in addresses. These are globally unique and so don't cause this kind of conflict. If you do need to use locally administered addresses, you must ensure that unique allocations are made to each host.
In lieu of applying a fix, we'll use a protocol analyzer to confirm our diagnosis with certainty.

Troubleshooting a security issue is often a complex task because there are many different systems that could be preventing access (or that are misconfigured to allow access when it should be blocked).
These systems include authentication, execute and configuration privileges for users and services, file system permissions/ACLs, network firewall ACLs, host firewall settings, and anti-malware/intrusion detection/data loss enforcement policies and modules. You need to know how to locate configuration information and how to access log data to diagnose these issues accurately.
Refer back to the troubleshooting model steps. Once you have diagnosed the problem, you must plan and implement a solution. Recall the CompTIA troubleshooting model steps. 
With the solution applied, recall the CompTIA model steps that complete the troubleshooting process:

 • Verify full system functionality and, if applicable, implement preventive measures.

 • Perform a root cause analysis.

 • Document findings, actions, and outcomes throughout the process.

And there we have it, Information regarding what was learned to achieve the troublehsooting badge for Server+ :)

Thank you for reading, I wish you the best, may your cybersecurity journey be filled with many great discoveries and growth of knowledge, remember to be ethical and moral in the descisions made, and how they impact those around you, we are building something now for the future of humanity, we owe it to ourselves to be the best version of ourselves we can, to aid in a joyus life experience full of discovery <3

Best Wishes and Sincerely,

Austin B.

The CompTia Server+ Troubleshooting badge covers exam objectives in sections, 4.1, 4.5, 4.6 .

##

##
