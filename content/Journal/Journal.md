---
title: Journal
draft: false
tags:
---
Back to the [[Central Hub]]

## **A history of edits to the site**

--- 
# 11/09/2025

Site Updates & Housekeeping

I’ve been doing some tidying up around the site lately and wanted to share a quick update on what’s new.

- **Improved Readability**: I went back to [[1.1 The OSI Model]] and added proper headings. It’s much easier to follow now instead of being one long wall of text.
- **Better Mobile Navigation**: Since the site can feel a little cramped on smaller screens, I added some extra links to make it easier to move around when browsing on mobile.
- **New Page – Inspiration & Quotes**: I’ve carved out a space dedicated to motivation, ideas, and quotes worth holding onto.
- **Linux Section**: There’s now a dedicated Linux area for general notes and learnings. This is separate from the CompTIA material so I can keep things better organised.

Nothing too flashy, just some behind-the-scenes improvements to make the site cleaner and more useful as it grows

---
# 27/08/2025
I’ve started working through a Python tutorial video and decided to write my notes online as I go. My knowledge of Python is pretty basic, I’ve done a bit of coding with it before but I really wanted to start from scratch and build a stronger foundation.

So far, I’ve covered:
- **Why Python matters** and what makes it such a popular programming language. 
- **How Python is installed** and set up on a system.
- An introduction to the **interpreter** and how it processes code.
- Exploring different **code editors** and choosing the right one for learning.
- Writing my **first simple Python program**.

It feels good to slow down and really understand the fundamentals this time. I’m excited to keep building on these basics and see how far I can take this learning journey.

I’ve also found a couple of errors on the site, so I’ll be going back to comb over what I’ve already done. That means fixing backlinks, tidying up index pages, and fleshing out the skill tree page a bit more. It feels like part of the same learning process, improving not just my coding, but also the way I organize and present what I’m working on.

---
# 19/08/2025

Made a start on a _Level Up_ section to the site, a road map of where I’m heading and an attempt at time blocking. The idea is to treat it as both a progress tracker and a bit of accountability for myself. Writing things down makes them feel more real, less like abstract goals floating in my head.

Time blocking is still new to me, so I’m approaching it more as an experiment than a strict system. The goal isn’t to fill every minute but to give my days some structure so I can see where the time goes and hopefully direct more of it toward the things that matter.

I’ve also started experimenting with **Mermaid charts in Obsidian** to map things visually. They’re really handy for sketching out timelines and workflows, but I’m not 100% sure yet how well they’ll render once pushed to the web. Hopefully they translate cleanly, because they could add a nice visual layer to the _Level Up_ roadmap.

This section of the site will probably evolve over time. Right now, it’s a starting point, a rough sketch of what I want to accomplish and how I plan to get there. I’m curious to see how it changes as I learn what works and what doesn’t.

The _Level Up_ page feels like a small step, but it’s an important one. It’s not just about productivity—it’s about documenting the process of growth, experimenting with tools and systems, and learning from the journey along the way.

---
# 14/08/2025

**Guess Who’s Back?**

After being offline for the better part of 8 months, the site is finally back in action!

What happened? Well… it started with a noble goal. I wanted to make things simpler: edit everything from my main Obsidian vault, have it magically sync, and drop a fresh copy of my content folder straight into my VS Project folder. Easy, right?

In theory, yes. In practice… I accidentally built a file-duplicating feedback loop that behaved suspiciously like a computer virus. (10/10 would _not_ recommend.)

The site itself was never actually down it just became impossible for me to update it. My local copy got completely trashed. Thankfully, the GitHub version was safe and untouched, patiently waiting for me to sort myself out.

To get things back on track, I had to tackle a whole to-do list and pick up some new skills along the way:

- How to pull a copy of my project using the GitHub extension in VS Code
- How to add and remove an origin
- How to add and remove an upstream to track updates
- How to check if my origin and upstream configurations are correct
- How to install all required dependencies for the project using npm
- How to set my author ID
- How to generate SSH keys and add my public key to GitHub
- How to build and serve the site locally for review before publishing changes

It took some work (and a few “aha” moments), but we’re back. Lesson learned: sometimes “making it simpler” makes it _way_ more complicated before it gets better.

---

# 03/12/2024
- made a very small start on Linux+ notes
	- started a section on regular expressions

- **Before AI**
	- Due to many requests, grammar has been corrected on the index page and all pages going under final review (not including drafts) will be run through Grammarly

- **After AI**
	- Due to many requests, the grammar has been corrected on the index page. All pages going through the final review process (excluding drafts) will be checked with Grammarly.
- *Technically this correction was made with my self-hosted LLM*

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
- Spent some time poking around sites, videos, and chats surrounding LLMs
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



Back to the [[Central Hub]]
