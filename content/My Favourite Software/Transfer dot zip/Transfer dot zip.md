---
title: Transfer dot zip
draft: false
tags:
---
 # Transfer dot zip
currently Installed on: Have not tried the selfhosted program yet, only used it through the browser
[Link to the site](https://transfer.zip)
(Link to the selfhosted program on Github)[https://github.com/robinkarlberg/transfer.zip-web]
![[Pasted image 20241130093131.png]]

I first stumbled upon transfer.zip because of a problem our gaming group encountered, there was a need to frequently share large (500Mb+) zip files containing car and track models for the racing sim Assetto Corssa. 

We threw around some ideas, I had previously used Firefox send and remembered it had an extremely large limit and was reported to be secure, unfortunately it was decommissioned in 2020.

Discord is usually good for this but has a 50mb limit, it was looking like drop box or google drive was the way to go, we noted a lot of time would be lost waiting for the file to be uploaded but could be negated if files were uploaded in advance. Due to the spontaneous nature of sessions we would rarely get to upload in advance.

I considered using the command line, OpenSSH, a Basic HTTP/FTP Server or rsync on WSL (Windows Sub-system for Linux) but all of these options would require authentication, encryption, firewall configuration if done correctly. A real possibility but a fair bit of effort to go to.

While searching I found transfer.zip based on WebRTC, it turned out to be a simple, turn key, secure solution to our problem. It worked first try, didn't require us to sign up to an account and best of all because its p2p there was no waiting for an upload before downloading! Problem solved.

**Overview:** Transfer.zip is a self-hostable web application designed for secure, quick, and unlimited file transfers between devices. It uses WebRTC for peer-to-peer file sharing and avoids the complexity and size limits of traditional platforms like Google Drive or Dropbox. The application is particularly suited for temporary file sharing without storage, making it ideal for scenarios like sharing large WAV files.

**Key Features:**

- **Quick Share:**
    - Utilizes WebRTC for end-to-end encrypted, peer-to-peer file transfers.
    - Files are streamed directly between devices, bypassing storage on servers.
    - Encryption uses AES-GCM with a 256-bit key, ensuring privacy.
    - File sharing is simple via QR codes or shareable links.
    - No size or bandwidth limitations.

- **Quick Share Relay:**
    - A fallback option when WebRTC is blocked by firewalls.
    - Uses a signalling server as a relay to bypass network restrictions.

- **Permanent Transfers (Planned):**
    - While currently unavailable in the self-hosted version, future updates may include support for permanent file storage via an open-source API.

**Limitations:**
- Issues with 0-byte files getting stuck during transmission.
- Compatibility challenges with some browsers:
    - Firefox Mobile: File transmission issues.
    - Safari: WebSocket connection problems when the window is unfocused.

**Use Case:** Ideal for users who prioritize seamless, temporary file transfers without the need for permanent storage or size restrictions. The tool is easy to self-host and open for contributions.