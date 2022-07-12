---
title: "Rule Based Targeting"
chapter: true
weight: 18
---

## Rule Based Targeting

In our previous exercise we leveraged user targeting to "dark launch" a feature to a specific user. This is helpful when working with smaller development teams, or an debugging with a specific user - but in order to scale the way features are released to users, you'll want to understand the concept of targeting rules. 

Targeting rules in LaunchDarkly can be used to rollout a feature to user cohorts based on a variety of properties. They can also be used to configure "segments" of users, or predefined cohorts such a "Dev Users" or "West coast users" that can be reused across multiple feature flags. 

In this exercise we'll create a targeting rule for another feature flag, and roll it out to users who match a specific configuration. 

<table class="credit">
<tr class="credit"><td class="credit" style="width:100%">
{{% notice note %}}
Want to see the feature flag in code? You can see the flag we are creating in this step [here on line 33](https://github.com/launchdarkly-labs/ld-aws-devops-workshop/blob/f14b5aed952035cc22161c366ee06a3c686352ba/src/App.js#L33). Remember, you can view this in an IDE by pressing the . key within the GitHub repository. 
{{% /notice %}}
</td></tr>
</table>

1. Return to your LaunchDarkly dashboard and click [**Create flag**](https://app.launchdarkly.com/default/test/features/new), this will open a tab for configurations for the flag. 
![Create Service](/images/setup/rule-target-0.png)

1. Name the feature flag `cardshow` (which will also populate the Key with the `cardshow` value). Provide a description, and check the box for [*SDKs using Client-side ID*](https://docs.launchdarkly.com/home/getting-started/feature-flags#making-flags-available-to-client-side-and-mobile-sdks). The rest of the page can be optionally filled out. Once you've completed, select **Save flag** on the bottom.
![Card Flag](/images/setup/rule-target-1.png)

1. Within the feature flag configuration screen, select **Add rules**. Provide a name for your rule (optional) and observe the rule configuration menus. In the *Select an attribute* drop down, select `device`. In the *Enter some values* drop down, select or enter `browser`, and in the final box set the value to `true`
![Add rule target](/images/setup/rule-target-2.png)
 
1. Scroll down to the **Default rule** section and set SERVE to **false**. This will ensure that all users accessing the application by default have the feature disabled. 
![Set default rule](/images/setup/user-target-2.png)

1. Return to the top of the page and enable your feature flag, and select **Review and save**, confirm and accept your changes. Observe that the cards view highlighting "Release" now displays. This rule is configured to display only on Web Browsers, and will not render on mobile device browsers. 
![Enable targeting](/images/setup/rule-targeting-demo.gif)

Learn more about using the targeting rules in [LaunchDarkly documentation](https://docs.launchdarkly.com/home/flags/targeting-rules).