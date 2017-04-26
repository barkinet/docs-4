---
title: "Disabling the AWS Lambda Integration"
---
If you decide to disable the AWS Lambda integration for any reason, you can accomplish this from the ["Integration Settings"](https://snyk.io/org/snyk/manage/integrations) page in your settings.

You'll need to find the AWS Lambda integration in your list of integrations, and click "Edit Settings". You'll be taken to a page that shows the current status of your AWS Lambda connection, a place to update your API key, and a red box at the bottom to disconnect from AWS Lambda.

![Screenshot showing the Disconnect screen for disabling the AWS Lambda integration](http://res.cloudinary.com/snyk/image/upload/c_scale,q_auto,w_auto/v1493156542/serverless-docs/aws-disconnect.png)

If you choose to disconnect, your AWS Lambda credentials will be removed from Snyk and any AWS Lambda projects we had been monitoring will be deactivated on Snyk.

If you choose to re-enable the AWS Lambda integration at any time, you'll need to re-enter your credentials and active your projects.

