---
title: "Fixing Ruby projects"
---

Currently we only support fixing Ruby projects through our GitHub integration. We fix by updating vulnerable gems, using `bundle update`, after modifying your Gemfile (sticking to the rules you have specified there as far as possible). This means that in some scenarios we won’t be able to upgrade all dependencies to non-vulnerable versions. In this case, you should consider updating the rules in your Gemfile. In future releases, we are planning to provide suggestions to make this easier.
