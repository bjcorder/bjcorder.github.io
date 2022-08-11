---
layout: post
title: "Installing CrowdSec Agent"
date: 2022-08-11 09:00:00 -0500
categories: [documentation,configuration]
tags: [security,crowdsec]
---

Operating System: Red Hat Enterprise Linux 8.6

Operating System: Ubuntu Server 22.04

# Installation

## Red Hat Enterprise Linux 8.6

Install the CrowdSec repositories to get access to the most recent packages for the CrowdSec agent and Bouncers:

```bash
curl -s https://packagecloud.io/install/repositories/crowdsec/crowdsec/script.rpm.sh | sudo bash
```

Install the CrowdSec agent from the repository:

```bash
sudo dnf install crowdsec
```

Install the basic firewall Bouncer:

```bash
sudo dnf install crowdsec-firewall-bouncer-iptables
```

Finally, enroll the instance to your CrowdSec account:

```bash
sudo cscli console enroll {YOUR_INSTANCE_TOKEN}
```

## Ubuntu Server 22.04

Install the CrowdSec repositories to get access to the most recent packages for the CrowdSec agent and Bouncers:

```bash
curl -s https://packagecloud.io/install/repositories/crowdsec/crowdsec/script.deb.sh | sudo bash
```

Install the CrowdSec agent from the repository:

```bash
sudo apt install crowdsec
```

Install the basic firewall Bouncer:

```bash
sudo apt install crowdsec-firewall-bouncer-iptables
```

Finally, enroll the instance to your CrowdSec account:

```bash
sudo cscli console enroll {YOUR_INSTANCE_TOKEN}
```