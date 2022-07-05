---
title: "5. LaunchDarkly - Your First Feature Flag"
chapter: true
weight: 18
---

In order to leverage LaunchDarkly, we need to configure Feature Flags that can be toggled on or off. One half of this configuation lives within your application code, and the other half lives within the LaunchDarkly platform. In this section, we will create our first feature flag in LaunchDarkly. 

<table class="credit">
<tr class="credit"><td class="credit" style="width:100%">
{{% notice note %}}
Want to see the feature flag in code? You can see the flag we are creating in this step [here starting on line 16](https://github.com/launchdarkly-labs/ld-aws-devops-workshop/blob/f14b5aed952035cc22161c366ee06a3c686352ba/src/App.js#L16). Remember, you can view this in an IDE by pressing the . key within the GitHub repository. 
{{% /notice %}}
</td></tr>
</table>

## Create and Release Your First Feature Flag
1. Return to your LaunchDarkly dashboard and click [Create flag](https://app.launchdarkly.com/default/test/features/new), this will open a tab for configurations for the flag. 
![Create Service](/images/setup/create-flag-1.png)

1. Name the feature flag `prodHeader` (which will also populate the Key with the `prodHeader` value). Provide a description, and check the box for "SDKs using Client-side ID". The rest of the page can be optionally filled out. Once you've completed, select "Save flag" on the bottom.
![Create Service](/images/setup/create-flag-2.png)
{{% notice info %}}
   The feature flag key must be named **prodHeader** to match what's in the deployed application
{{% /notice %}}

1. Turn on the feature flag and see the feature release in real-time
![Create Service](/images/setup/flag-demo.gif)