## Description 
In the case where you have a forked a repo and secrets such as `APP_ID` or `APP_PRIVATE_KEY` are used in an existing feature or Github action that 
you want to test in your personal fork or you want to test a new feature/action which uses theses secrets in your fork, this process outlines successfully used steps. 
These secrets although they may be setup for the source repo, are not normally passed along to forks and thus some setup is required

## Steps
### 1. Create sample Github app
Flow steps [here](https://docs.github.com/en/developers/apps/building-github-apps/creating-a-github-app) to create a sample Github app for your account
* Homepage URL can simply be your fork's github link
* Disable Webhook unless explicitly needed
* Permissions will vary based on use case, but in cases of say backporting we would need the ability to both create and delete branches as shown below:


After creating in the "General" tab you will see your "App ID" listed and its value will be the contents of your `APP_ID` secret


### 2. Upon creation, follow banner (or find) and "Generate Private Key"
This is required for installing your Github app and its private key contents (which get downloaded) will be the contents of the `APP_PRIVATE_KEY` secret


### 3. Install App to your account
In the "Install App" tab you will need to install the app to your account to later be able to use in your personal repos

### 4. 
