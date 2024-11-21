---
title: NAS Revamp
draft: false
tags:
---
 
I have a NAS (Network Attached Storage) based on Open Media Vault running on a Raspberry pi and its been great, I installed and configured it around mid 2022 when I needed a central location to store files I was accessing from different computers, mainly video files. Initially it was running on a Pi 3 and soon after installing Plex server I realised it needed a little more grunt so I purchased a Pi 4 and its been great ever since, until it wasn't.

Its been a capable little unit, reliably serving content with settings as high as 4k 60fps locally around my network. There is plenty it cant do, like encoding for delivery remotely or relied upon for storage of important files, which brings me to the main issue.

I believe the SD card the whole thing runs on is on its last legs, issues have started appearing such as database corruption in Plex and recently the Open Media Vaults front end wont load and fails with an error so its time to rebuild it.

Far from a solid, fault tolerant solution, a mac mini with USB drives attached isn't ideal but it is cheep when inherited and better than what I have currently. This configuration is hotly debated online and discouraged, the reasons listed have not been enough to discourage me.

- *Post link I found to article* 
- *outline reasons my plan is not optimal*



## The OS
Open Media Vault was a good choice, it ran reliably on low end hardware and was easy to install configure

## Hardware
- Apple Mac mini
	- version
	- ram
	- hd
	- attached hard drives
		- raid? prob not a good idea as the drives will be attached by USB
			- syncthing for redundancy?
- reliability testing of second hand equipment
	- been running Ubuntu server
		- minecraft server
			- dynmap has been maxing the unit for days at a time without issue
				- in hindsight i should have been logging data like temps and system resource use

Network
- wired
	- static IP/reservation

Security
- secure unique passwords for all accounts
- encryption?
- snapshots?

## Input From a Professional

- **Compare snapshots and backups**:
    - Understand that snapshots act as pointers to a state in time.
    - Investigate the importance of quiescing when creating snapshots to ensure data consistency.
    - Recognize that backups allow for full restoration of data, providing a complete recovery solution.

- **Security considerations**:
    - Explore the concept of immutable backups.
    - Research how immutable backups can protect against ransomware attacks by preventing unauthorized modifications.

- **Research expansion**:
    
    - Identify scenarios where snapshots are sufficient versus when full backups are necessary.
    - Look into tools and methods for implementing secure, immutable backup systems.
    - Evaluate the role of snapshots and backups in disaster recovery planning. 

