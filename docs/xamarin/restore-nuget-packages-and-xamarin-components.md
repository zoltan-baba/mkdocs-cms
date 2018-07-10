# Restore NuGet packages and Xamarin Components

To restore your [NuGet](https://www.nuget.org/) packages or [Xamarin Components](https://components.xamarin.com/) simply navigate to the app on [bitrise.io](https://www.bitrise.io), and select the `Workflow` tab to open the Workflow Editor.

## Restore Nuget packages

Add the `NuGet Restore` step to your workflow, after the `Git Clone` step. By default the step will use the same solution file that you have provided when you added your app, but you can simply modify it if you need to.

## Restore Xamarin Components

Add the `Xamarin Components Restore` step, after the `Xamarin User Management` step.

**Xamarin Components requires Xamarin authentication - for more information please see the** [**Connect your Xamarin account to Bitrise**](https://github.com/OrganizationDummy/devcenter/tree/acf5f40e38b6dcf6fe62e839a4c04acb31fdebd2/xamarin/connect-your-xamarin-account-to-bitrise/README.md) **guide!**

