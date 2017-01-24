---
title: Troubleshooting
---

If your instance of the Snyk CLI has started failing, follow these steps to resolve:

1. Ensure you are on the most up to date version of the CLI by running

	 ```console
   npm update -g snyk
   ``` 
2. Make sure you are authenticating prior to running the Snyk CLI command

  You can either authenticate by running snyk auth in your terminal, and it’ll guide you through this process, or visit https://snyk.io/account copy your API token and paste it into your terminal as follows:
  ```console
   snyk auth <your token>
   ``` 

3. If you are still having problems after upgrading and authenticating send an email to support@snyk.io and we will try to help you out. 

###Note:
Authentication is required for snyk test and snyk monitor from Tuesday the 24th of January 2017 for details on why we require authentication take a look at https://snyk.io/blog/requiring-authentication/  

Registration with Snyk is free. If you do not already have an account all you need to do is run `snyk auth` in your terminal (or register on https://snyk.io/) to get an account setup.
