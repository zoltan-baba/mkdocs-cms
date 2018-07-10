# Adding an Assembla webhook

You can set up webhooks so that Bitrise automatically triggers a build of your app whenever you perform a specified action, such as a code push or a pull request. For Assembla, you only need to add your `bitrise-webhooks` URL to your [Assembla](https://assembla.com) space.

## Get the webhook URL for Assembla

1. Navigate to the `Code` tab of your app's page and select `Assembla` from the dropdown menu of the `Incoming Webhooks` section.

   ![Screenshot](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/webhooks/bitrise-assembla-webhook.png)

2. Copy the webhook URL for the selected service.

## Set up webhook on Assembla

1. Open your space on [assembla.com](https://assembla.com) or your organisation's assembla domain.
2. Go to the `Webhooks` section of the space.
3. Select `Create New Webhook`.
4. Set `Title` to `BitRise Webhook`.
5. Specify the `bitrise-webhooks` URL. \(`.../h/assembla/BITRISE-APP-SLUG/BITRISE-APP-API-TOKEN`\) in the `External url` field
6. Select `application/json` in the `Content type` field.
7. Paste the following code to `Content`:

   ```text
    {"assembla": {"space": "%{space}", "action": "%{action}", "object": "%{object}"}, "message": {"title": "%{title}", "body": "%{body}", "author": "%{author}"}, "git": {"repository_suffix": "%{repository_suffix}", "repository_url": "%{repository_url}", "branch": "%{branch}", "commit_id": "%{commit_id}"}}
   ```

8. Select `Code commits` and/or `Git Push` in the `Post updates about:` section.
9. Click `Add`.

That's all! The next time you **push code** a build will be triggered \(if you have Trigger mapping defined for the event\(s\) on Bitrise\).

