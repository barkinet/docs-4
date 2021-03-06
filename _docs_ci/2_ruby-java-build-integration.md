---
title: Ruby or Java CI integration
---

To continuously avoid known vulnerabilities in your Ruby or Java dependencies, integrate Snyk into your continuous integration (a.k.a. build) system. Here are the steps required to to so:

1. Install the Snyk utility using `npm install -g snyk`.
2. Add `snyk test` to your CI test platform
3. Configure your environment to include the `SNYK_TOKEN` environment variable. You can find your API token in your [account settings on snyk.io](https://snyk.io/account/).

To stay secure over time, Snyk alerts you about newly disclosed vulnerabilities that affect your project's dependencies.
To make sure the list of dependencies we have for your project is up to date, refresh it continuously by running `snyk monitor` in your deployment process.
