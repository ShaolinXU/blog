+++
date = '2025-07-09T22:57:07+02:00'
draft = false
title = 'Configure Rdp Ubuntu'
+++

After configure the remote login on ubuntu, I still cannot connect to my ubuntu server using Windows App on my mac. After searching I found the following solution from reddit: [link](https://www.reddit.com/r/Ubuntu/comments/1c40ei8/comment/lhzgbk8/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button)

```bash
From Microsoft RDP export the RDP.

Open the file.rdp with your text editor

Find: use redirection server name:i:0

Change to: use redirection server name:i:1

Save

Drag back to Microsoft RDP and open

```