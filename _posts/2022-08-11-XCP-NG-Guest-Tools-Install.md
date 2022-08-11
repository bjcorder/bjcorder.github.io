---
layout: post
title: "Installing the XCP-NG Guest Tools"
date: 2022-08-11 10:00:00 -0500
categories: [documentation,configuration]
tags: [rhel,linux,os,repo,ubuntu,xcp-ng]
---

Operating System: Red Hat Enterprise Linux 8.6

Operating System: Ubuntu Server 22.04

# Installation

## Red Hat Enterprise Linux 8.6

Make sure that the EPEL repositories have been installed as shown in [this post]({% post_url 2022-08-11-RHEL-8_6-EPEL %}).

First, update all of your repositories:

```bash
sudo yum update
```

Install the Guest Utilities from the EPEL repository:

```bash
sudo yum install xe-guest-utilities-latest
```

Finally, make sure to enable and start the Guest Utilities service, and then reboot the system.

```bash
sudo systemctl enable xe-linux-distribution
sudo systemctl start xe-linux-distribution
sudo reboot now
```

## Ubuntu Server 22.04

First, update all of your repositories and upgrade all packages:

```bash
sudo apt update && sudo apt upgrade -y
```

Install the Guest Utilities:

```bash
sudo apt install xe-guest-utilities
```

Once completed, restart the server:

```bash
sudo reboot now
```