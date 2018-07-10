# Deploy your Xamarin app

After successfully adding your Xamarin application we will create a default workflow \(build configuration\) for you. This workflow includes a `Deploy to bitrise.io` step by default.

Building the default workflow will checkout your git repository, archive your application and move all the generated applications \( `ipa` / `apk` \) to the deployment folder. After the archive the `Deploy to bitrise.io` step will upload these files to Bitrise.

We will not just upload your application, but send out an email to your team as well. They can simply open the email from their mobile device and install the application from there. Also you can send out the build to any tester by providing their email address.

## But what if you are already using or want to use another deployment service?

Besides the default Bitrise deployment we have [dozens of other services integrated](http://www.bitrise.io/integrations#?filter=deploy) to Bitrise. You can simply modify your workflow and add the ones you would like to, like [HockeyApp](http://hockeyapp.net/), [Appaloosa](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/tutorials/deploy/publish-your-app-to-appaloosa/README.md) or [TestFairy](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/tutorials/deploy/deploy-to-testfairy-with-bitrise/README.md) - just filter by the `deploy` tag in the list to see all the available deployment steps.

Simply add the integration Step you want to use instead of the `Deploy to bitrise.io` step or after that \(but in any case after the `Xamarin Archive` step, as that's the step which generates the deployable artifact - `.ipa`, `.apk`, ...\), and fill out the parameters of the step.

The next time you start a build your app will be deployed to the service of your choice!

## Code signing

### Xamarin.Android

For Xamarin Android project code signing see the [Create signed APK on bitrise.io](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/android/code-signing/README.md) tutorial.

### Xamarin.iOS

**Work in progress** - this section will be updated soon.

Right now the best way to get started with Xamarin.iOS code signing is to run [codesigndoc](https://github.com/bitrise-tools/codesigndoc#one-liner) and upload the files it generates, or to manually upload the code signing files you use locally.

_Code signing files can be uploaded to_ [_bitrise.io_](https://www.bitrise.io) _in the app's Workflow Editor, under the_ `Code signing & Files` _section of the editor._

