---
title: Fixing vulnerabilities
---
### What can I do if I’m vulnerable?

If possible, the cleanest and best way to address a vulnerability is to upgrade to a vulnerability-free version of the package you’re using. In most cases, disclosed vulnerabilities are fixed shortly after they’re discovered, and all you need to do is **upgrade to the relevant version.**

- For Node.js and Ruby GitHub repos, you can [generate a pull request](https://snyk.io/docs/github/#fix-vulnerabilities-with-snyk-pull-requests) to upgrade. 
- For Node.js projects, you can use Snyk's CLI [`wizard`](https://snyk.io/docs/using-snyk/#wizard).

If you can’t upgrade, because there is no sufficient direct upgrade available, or because the upgrade includes breaking changes you can’t take on right now, your next best option is to **apply a patch.** A patch changes the locally installed package file to fix the vulnerability.

- For Node.js projects, you can apply patches either via a [GitHub pull request with fixes](https://snyk.io/docs/github/#fix-vulnerabilities-with-snyk-pull-requests), or by running Snyk [`wizard`](https://snyk.io/docs/using-snyk/#wizard).
- Patching is currently not supported for Ruby. You can open a pull request to ignore vulnerabilities that can't be fixed. 

### What does patching mean?

A patch will make the minimum changes required to your locally installed package files, to fix the vulnerability. Patching is a good option to fix vulnerabilities when you can’t upgrade.
If you’re monitoring your project, we will notify you once an upgrade becomes available.
Note that patching isn't supported yet for Ruby projects.

### Can patching break my code?

We test all patches we release rigorously, and keep the changes a patch makes to your code to a minimum. We haven’t seen a single case where our patches broke intended functionality. However, we can’t guarantee that a patch won’t break something. If you are unsure, it’s best to take a look at the patch before applying it.

### When I can choose, how should I decide whether to upgrade or patch?

An upgrade is usually the best way to fix a vulnerability. If both an upgrade and a patch are available, Snyk will usually recommend the upgrade. 

- Our GitHub integration will suggest the best fix available. If there is both an upgrade and a patch, the fix pull request will recommend to upgrade. 
- If you're using Snyk's CLI for Node.js, Snyk [`wizard`](https://snyk.io/docs/using-snyk/#wizard) lets you choose to patch, even if an upgrade is available. You might want to patch if an upgrade would be a potentially breaking change (we highlight if this is the case), or if you have other reasons to not upgrade for now.

If you’re unsure and would like to assess the impact before applying a fix, check Snyk's advisory for the vulnerability.

### What if there is no upgrade or patch available?

Assess the issue, and weigh up risk against effort. If the risk is high, you could remove the dependency. You can ignore the vulnerability for 30 days (by opening a pull request, or via `snyk wizard`); Snyk will ask you again what to do in 30 days time. If you watch the project, we will notify you if any upgrades or patches become available.

If you decide that the vulnerability is not an issue (for instance, because a component is not really deployed to production), you can manually edit the Snyk policy (.snyk) file to use a far-future expiry date for this instance. 
