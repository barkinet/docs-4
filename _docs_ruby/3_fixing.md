---
title: "Fixing Ruby projects"
---

We fix by updating vulnerable gems, using `bundle update`, without changing your Gemfile (sticking to the rules you have specified there). This means that in some scenarios we won’t be able to upgrade dependencies to a non-vulnerable version. In this case, you should consider updating the rules in your Gemfile. In future releases, we are planning to provide suggestions to make this easier. 
