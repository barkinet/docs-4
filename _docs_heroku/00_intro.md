---
title: ""
---

Snyk's Heroku integration lets you monitor the deployed code of your Node.js and Ruby Heroku applications for any known vulnerabilities found in the application's dependencies, testing at a frequency you control.

For each test, Snyk will communicate directly with Heroku to determine exactly what code is currently deployed and what dependencies are being used. Each dependency will in turn be tested against Snyk's vulnerability database to see if it contains any known vulnerabilities. 

If vulnerabilities are found, you will be alerted (via email or Slack) so that you can take immediate action.

In order to turn on the Heroku integration you'll need to:

1. [Connect to Heroku](#connecting-snyk-to-heroku) from the integrations page
2. [Add your Heroku API token](#generating-your-heroku-api-key) to Snyk
3. [Select the projects you want to monitor](#adding-heroku-projects-to-snyk) and click "Add to Snyk"