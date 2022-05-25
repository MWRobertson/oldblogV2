---
layout: post
title: Get-SiteCodeCoverage.ps1
tags: powershell gist activedirectory
---

Because the machinery of an enterprise network moves slowly, there could be a significant period between the point where you demote all of the domain controllers in an AD site and the point where your network architecture team is ready to retire the site itself. In the interm, I like to check to verify which domain controllers from a neighboring site have taken over responsibility for providing authentication services for the clients. 

The best way I've come up with for retrieving this information is by querying the LDAP and Kerberos SRV records for the retiring site in DNS. In an effort to automate that check, I've created a quick function called Get-SiteCodeCoverage. 

<script src="https://gist.github.com/MWRobertson/5a2bd201c336f7ac4615e216fcde80ba.js"></script>