---
title: ""
---

**What type of Ruby projects do we support?**

Ruby V1 supports scanning and fixing Ruby projects that have their dependencies managed by Bundler. You’ll also need to have your Gemfile.lock checked into the root of your repository. 
Support for gem libraries is in the pipeline. 
Snyk for Ruby is currently only available for GitHub repositories. 

**Testing Ruby projects**

We scan Ruby projects by examining your Gemfile.lock to compare the specific versions of every [direct and deep dependency](https://snyk.io/docs/faqs/#about-known-vulnerabilities) in your project against our Ruby vulnerability database.
We are testing all Bundler groups, and currently you can’t choose to exclude certain groups (such as test or development groups). 

**Fixing Ruby projects**

We fix by updating vulnerable gems, using `bundle update`, without changing your Gemfile (sticking to the rules you have specified there). This means that in some scenarios we won’t be able to upgrade dependencies to a non-vulnerable version. In this case, you should consider updating the rules in your Gemfile. In future releases, we are planning to provide suggestions to make this easier.  
