---
title: "Testing Java projects"
---
We scan Java projects by examining your pom.xml (and installed packages, when using the [CLI](/docs/using-snyk/)) to compare the specific versions of every [direct and deep dependency](https://snyk.io/docs/faqs/#about-known-vulnerabilities) in your project against our [Maven vulnerability database](/vuln?type=maven).
We ignore test dependencies by default, but they can be included from the [CLI](/docs/using-snyk/).
