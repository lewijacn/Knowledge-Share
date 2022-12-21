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
<img width="374" alt="image" src="https://user-images.githubusercontent.com/16884063/208951845-d65dc8e0-6718-4d77-894e-de4a3c3ce62f.png">



After creating in the "General" tab you will see your "App ID" listed and its value will be the contents of your `APP_ID` secret


### 2. After creation, follow banner (or find) and "Generate Private Key"
This is required for installing your Github app and its private key contents (which get downloaded) will be the contents of the `APP_PRIVATE_KEY` secret


### 3. Install App to your account
In the "Install App" tab you will need to install the app to your account to later be able to use in your personal repos

### 4. Selecting desired repos
If you have configured Repository permissions, its time to select applicable repos

Go to your Profile -> Settings -> Applications (Under "Integrations") -> Configure (Sample Github App) -> Select repos (Under "Repository Access")

### 5. Updating permissions
Any time the permissions change for a Github App, these changes must be reviewed and accepted before they will be enacted for the account
* This can be done in the applicable repo settings or your own account settings

<img width="816" alt="image" src="https://user-images.githubusercontent.com/16884063/208951405-000c2c37-c576-428d-ad44-2182840bf66c.png">

