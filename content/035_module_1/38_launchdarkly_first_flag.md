---
title: "Your First Feature Flag"
chapter: true
weight: 17
---

## Create and Release Your First Feature Flag

{{% notice note %}}
   Want to see the feature flag in code? You can see the flag we are creating in this step [here starting on line 16](https://github.com/launchdarkly-labs/ld-aws-devops-workshop/blob/f14b5aed952035cc22161c366ee06a3c686352ba/src/App.js#L16). Remember, you can view this in an IDE by pressing the . key within the GitHub repository. 
{{% /notice %}}

1. Return to your LaunchDarkly dashboard and click [**Create flag**](https://app.launchdarkly.com/default/test/features/new), this will open a tab for configurations for the flag. 
![Create Service](/images/setup/create-flag-1.png)

1. Name the feature flag `prodHeader` (which will also populate the Key with the `prodHeader` value). Provide a description, and check the box for [*SDKs using Client-side ID*](https://docs.launchdarkly.com/home/getting-started/feature-flags#making-flags-available-to-client-side-and-mobile-sdks). The rest of the page can be optionally filled out. Once you've completed, select **Save flag** on the bottom.
{{% notice info %}}
   The feature flag key must be named **prodHeader** to match what's in the deployed application and [the variable definition in the code](https://github.com/launchdarkly-labs/ld-aws-devops-workshop/blob/f14b5aed952035cc22161c366ee06a3c686352ba/src/App.js#L12)
{{% /notice %}}
![Create Service](/images/setup/create-flag-2.png)
1. Turn on the feature flag and see the feature release in real-time
![Create Service](/images/setup/flag-demo.gif)

Learn more about using the feature flags in [LaunchDarkly documentation](https://docs.launchdarkly.com/home/flags).