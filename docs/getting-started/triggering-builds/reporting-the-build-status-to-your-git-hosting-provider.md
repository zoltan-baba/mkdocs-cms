# Reporting the build status to your git hosting provider

Bitrise can push back build status reports to your git hosting provider \(GitHub/GitLab/Bitbucket\). You only need to authenticate Bitrise to communicate towards the git hosting service. Apart from build status reports, this enables other operations, such as auto-registering SSH keys or Webhooks.

To do this, you need to specify a Service Credential User on the `Team` tab of your app on [bitrise.io](https://www.bitrise.io). You also need to make sure that this user has a connected account with the git hosting service of your choice on [bitrise.io](https://www.bitrise.io). This account will be used by Bitrise to communicate with the API of the git hosting provider.

Please note that status reports are sent only for automatically triggered builds, such as builds triggered by a code push or a pull request.

1. Make sure the account you wish to use is connected to the relevant hosting provider: go to the `Account settings` page of the account and check the `CONNECTED ACCOUNTS` menu on the left side.

   ![Connected account](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/getting-started/triggering-builds/connected-account.png)

2. Go to the `Team` tab of your app on [bitrise.io](https://www.bitrise.io).
3. Find the `Service credential User` menu and select the user with the connected account.

   ![Service credential user](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/getting-started/triggering-builds/service-credential.png)

4. Click the `Test the git connection` button to make sure the selected user's connection can be used for sending back the build status to the hosting provider.

