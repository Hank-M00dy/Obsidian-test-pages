---
title: Journal
draft: false
tags:
---
**A history of edits to the site**

# 03/12/2024
- made a very small start on Linux+ notes
	- started a section on regular expressions

---
# 01/12/2024
- working on the site remotely so this is a good opportunity to download a few of the larger LLMs
	- entered my test questions into the new LLMs
		- [[Llama 3.1 8b Results]]
		- [[Qwen 2.5 - 14b Results]]
		- 

---
# 30/11/2024
- Added new software [[Transfer dot zip]], fantastic direct p2p file transfer program
- Spent some time poking around sites, videos and chat surrounding LLMs
	- Findings here [[Self Hosted LLM]]

---
# 29/11/2024
- Mainly performed rearranging of the the files within the Obsidian vault, because every note is a file and every attachment is a separate file as well things get out of hand very quickly.
	- started nesting parts of the blog for better separation
		- If the site breaks this is probably why
	- ![[Pasted image 20241129232127.png]]
- Added a couple of Items to the software section
	- [[Obsidian]] was an obvious addition due to the amount I use it
	- [[Mousam]] is a beautiful weather app for Linux that I found recently
- used my improved method for updating the journal section on the main page for the first time, works really well, no improvement needed
- Watched a video where Network Chuck sets up a blog, this has a striking resemblance to my own site but set up in a different way [[Network Chuck Blog]]

---
# 19/11/2024
- formatted and filled gaps in my notes for 2 more sections and published
	- added [[1.6  network services]]
	- added [[1.7  Datacentre network architecture]]
- took 2 articles off draft in the projects section, need to embrace posting stuff before its finished
- made a small addition to [[CD DVD Recovery]], added observations about the condition of the media
- copied everything from the what's new section to the journal and edited this section down to 3 entry's
- now that the 3 most recent Journal entry's are being displayed on the main page I searched for a way of referencing [[Journal]] instead of copy pasting.
	- I found that Obsidian already has syntax for that
		- `![[page your referencing#Heading]]`
			- by changing the dates to headings instead of dot points I can just reference the date on the index page which gets rid of duplicate effort
			- eliminates the chance there will be discrepancies between 'what's new' and 'Journal'
- There is still the issue of text appearing on a new line in Obsidian but appearing on one line when published to the web
	- how it appears on the web
		- ![[Pasted image 20241120001816.png]]
	- how it appears in Obsidian
		- ![[Pasted image 20241120002048.png]]
	- In a video I watched recently from IT Pro TV "CompTIA Linux+: Using vi/vim to edit files" they mention that at the bottom of the screen vim displays how text is formatted, they revile that there are different ways a line feed is formatted
		- in Microsoft Office at the end of every line is a **CRLF**, Carriage Return Line Feed, terms that go back to the typewriter days
			- a **CR** (Carriage Return)was the act of the mechanical printing head returning to the beginning of the line, if you ever used an old type writer you may have grabbed the leaver to manually pull the head back to its starting position. 
			- a **LF** (Line Feed) was the roller advancing the paper by a set increment, moving down a line. An LF was often initiated by the **CR** unless you were correcting an error, bringing the carriage back part of the way would not initiate a **CR**
		- In the Unix world they only do a **LF** and its assumed you go back to the beginning.
			- it is my assumption that my issue stems from this, the markdown language is issuing an **LF** but the static site generator Quarts needs a **CRLF** to produce the same result.
		- This may also be the reason why when you open a document on windows its all one continuous line, its missing the line feeds.

---

# 12/11/2024
- The Explorer section displayed on the left of the screen appears as a numbered list, they appear like this because each section resides in a folder and iv numbered them to be in a specific order, I don't like how it looks so I'm removing it, should make it look a bit cleaner
	- ![[Pasted image 20241112191221.png]]

---

# 11/11/2024
- Added my first entry into the software category, Space Monger, read about it here [[My Favourite Software]]
	- Fixed an issue with this page, the text was wrapping around the image incorrectly, its like it wants to continue flowing after the image tag without starting a new line. I dont have this issue when starting a new line with a bullet point. Manually adding a new line between image and text fixed this issue
		- ![[Pasted image 20241111233351.png]]
	
- Learnt how to modify the graph view, with default settings the text was to large when zoomed in and was all bunched together making it unreadable
	- in VS Code I opened the Graph.tsx file within quartz/components and modified 3 settings, I'm pretty happy with how this now displays when zoomed in
		- ![[Pasted image 20241111233105.png]]
		- ![[Pasted image 20241112191348.png]]

---

# 4/11/2024
- Added a few more pages to my study notes in the Network+ section
	- [[1.1 The OSI Model]]
	- [[1.2 Network Topologies and Types]]
	- [[1.4 IP Subnetting]]
	- [[1.5 ports and protocols and encrypted alternatives]]
