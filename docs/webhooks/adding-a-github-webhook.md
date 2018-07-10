# Adding a GitHub webhook

You can specify webhooks so that Bitrise automatically triggers a build of your app whenever you perform a specified action, such as a code push or a pull request. For GitHub, all you have to do is register your `bitrise-webhooks` URL as a Webhook in your [GitHub](https://www.github.com) repository.

## Get the webhook URL for GitHub

1. Navigate to the `Code` tab of your app's page and select `GitHub` from the dropdown menu of the `Incoming Webhooks` section.

   ![Screenshot](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/webhooks/github-webhook-1.png)

2. Copy the webhook URL for the selected service.

## Set up webhook on GitHub

1. Navigate to your GitHub repository and select `Settings`.

   ![Screenshot](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/webhooks/github-webhook-2.png)

2. Select `Add webhook` under Webhooks.

   ![Screenshot](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/webhooks/github-webhook-3.png)

3. Paste the GitHub Webhook URL from Bitrise to the Payload URL.

   ![Screenshot](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/webhooks/github-webhook-4.png)

4. And on the same page, select `Let me select individual events`.

   ![Screenshot](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/webhooks/github-webhook-5.png)

5. Select `Pull request` and `Push`. After you are ready press the `Add webhook` button and you are ready to roll!

   ![Screenshot](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/webhooks/github-webhook-6.png)

