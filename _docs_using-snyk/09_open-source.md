---
title: Open source projects
---

<p>Tests against open source projects are free. If your source code is available publicly on the internet, you can set your project as open source by following these steps.</p>

1. If you haven't done so already, run `snyk monitor` in your terminal to create a project on Snyk
2. On the Snyk website, view your [projects](https://snyk.io/projects) and select the CLI project you just created
3. Click on "settings" from the right hand side of this page to change the project settings
4. Enter a git URI to the source code for your project where it says "Git remote URI".
    - On GitHub, click the "Clone or download" button and copy the URI
    - On Bitbucket, click the "Clone" button and copy the URI
    - For other source code management solutions, look for a URI that ends with `.git`
5. If we are able to verify that the URI points to a git repository then your project will be marked as open source and will no longer be tracked against your private project test usage.
