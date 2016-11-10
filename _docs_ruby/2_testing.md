---
title: "Testing Ruby projects"
---

We scan Ruby projects by examining your Gemfile.lock to compare the specific versions of every [direct and deep dependency](https://snyk.io/docs/faqs/#about-known-vulnerabilities) in your project against our [Ruby vulnerability database](/vuln?type=rubygems).
We are testing all Bundler groups, and currently you can’t choose to exclude certain groups (such as test or development groups).
