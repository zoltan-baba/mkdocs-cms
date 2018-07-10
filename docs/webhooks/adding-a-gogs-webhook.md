# Adding a Gogs webhook

You can set up webhooks so that Bitrise automatically triggers a build of your app whenever you perform a specified action. For Gogs, all you have to do is register your `bitrise-webhooks` URL as a Webhook in your [Gogs](https://gogs.io) repository.

## Get the webhook URL for Gogs

1. Navigate to the `Code` tab of your app's page and select `Gogs` from the dropdown menu of the `Incoming Webhooks` section.

   ![Screenshot](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/webhooks/bitrise-gogs-webhook.png)

2. Copy the webhook URL for the selected service.

## Set up webhook on Gogs

1. Open your project on your repository's hosting URL.
2. Go to `Settings` of the project.
3. Select `Webhooks`, `Add Webhook`, then `Gogs`.

   ![Screenshot](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/webhooks/gogs-webhook-select.png)

4. Specify the `bitrise-webhooks` URL \(`.../h/gogs/BITRISE-APP-SLUG/BITRISE-APP-API-TOKEN`\) in the `Payload URL` field.

   ![Screenshot](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/webhooks/add-webhook-gogs.png)

5. Set the `Content Type` to `application/json`.
6. A Secret is not required at this time.
7. Set the trigger to be fired on `Just the push event`.

   ![Screenshot](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/img/webhooks/gogs-webhook-triggered.png)

8. Click `Add Webhook`.

And you're done! From now on, every code push to your Gogs repository will trigger a build on Bitrise.

