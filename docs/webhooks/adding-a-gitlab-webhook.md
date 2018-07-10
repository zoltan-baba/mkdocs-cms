# Adding a Gitlab webhook

You can set up webhooks so that Bitrise automatically triggers a build of your app whenever you perform a specified action, such as a code push or a pull request. For GitLab, all you have to do is register your `bitrise-webhooks` URL as a Webhook in your [GitLab](https://www.gitlab.com) repository.

## Get the webhook URL for GitLab

1. Navigate to the `Code` tab of your app's page and select `GitLab` from the dropdown menu of the `Incoming Webhooks` section.

   ![Screenshot](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/webhooks/bitrise-gitlab-webhook.png)

2. Copy the webhook URL for the selected service.

## Set up webhook on GitLab

1. Open your project on [GitLab.com](https://www.gitlab.com)
2. Go to `Settings` of the project.
3. Select `Integrations`.

   ![Screenshot](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/webhooks/integrations-gitlab.png)

4. Enter the bitrise-webhooks URL in the URL field.

   ![Screenshot](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/webhooks/gitlab-webhook-url.png)

5. In the `Trigger` section select:
   * `Push events`
   * `Tag push events`
   * `Merge request events`

     ![Screenshot](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/webhooks/gitlab-webhook-events.png)
6. Click `Add webhook`.

That's all! The next time you push code, push a new tag or create/update a merge request a build will be triggered \(if you have Trigger mapping defined for the event\(s\) on Bitrise\).

