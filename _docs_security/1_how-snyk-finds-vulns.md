---
title: How Snyk finds out about new vulnerabilities
---

Snyk's security team, based in Israel, maintains our vulnerability database. 

This work includes curating vulnerabilities found or reported elsewhere on the web, as well as doing our own research to uncover previously unknown vulnerabilities, which we then responsibly disclose. Snyk Enterprise get early notifications for issues our research uncovers alongside this responsible disclosure process.

Most of the vulnerabilities in our database originate from one of these sources:

* *Monitoring other vulnerability databases*, such as CVEs from [NVD](https://nvd.nist.gov/) and many others.
* *Monitoring user activity on GitHub*, including issues, PRs and commit messages that may indicate a vulnerability.
* *Bulk research*, using tools that look for repeated security mistakes across open source package code
* *Manual research*, investing our researchers time to manually audit more widely used packages for security flaws.

For every issue deemed to be a real vulnerability, we assign the right CVSS (severity) score and package version specification, create an advisory, and make it available in the product. 
