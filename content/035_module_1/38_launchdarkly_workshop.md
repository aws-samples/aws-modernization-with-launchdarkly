---
title: "5. LaunchDarkly Feature Management"
chapter: true
weight: 18
---

## Create and Release Your First Feature Flag
1. 
![Create Service](/images/setup/create-flag-1.png)
Return to your LaunchDarkly dashboard and click [+FLAG](https://app.launchdarkly.com/default/production/features/new), this will open a tab for configurations for the flag. 

2. 
![Create Service](/images/setup/create-flag-2.png)
Name the feature flag `show-widgets` and the Key `show-widgets`, check the box for "SDKs using Client-side ID". Finally, hit SAVE FLAG
{{% notice info %}}
   The feature flag key must be named **show-widgets** to match what's in the deployed application
{{% /notice %}}

3. Turn on the feature flag and see the feature release in real-time
![Create Service](/images/setup/flag-demo.gif)