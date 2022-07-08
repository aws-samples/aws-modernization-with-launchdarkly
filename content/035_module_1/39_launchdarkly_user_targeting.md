---
title: "6. LaunchDarkly - Introducing User Targeting"
chapter: true
weight: 18
---

## Feature Flagging - Introducing User Targeting 

In our previous exercise we enabled a LaunchDarkly feature flag that changed the visual look of our application. We can see a new banner displayed, as well as a logon box. 

The ReactJS based application that is currently running in AWS App Runner supports targeting based on several properties 

- The entered user name in the logon box 
- The device OS connecting to the application
- The browser type connecting 

In this exercise, we will configure a second flag that will render a graphic based on the targeted user.

<table class="credit">
<tr class="credit"><td class="credit" style="width:100%">
{{% notice note %}}
Want to see the feature flag in code? You can see the flag we are creating in this step [here on line 24](https://github.com/launchdarkly-labs/ld-aws-devops-workshop/blob/f14b5aed952035cc22161c366ee06a3c686352ba/src/App.js#L24). Remember, you can view this in an IDE by pressing the . key within the GitHub repository. 
{{% /notice %}}
</td></tr>
</table>

1. Return to your LaunchDarkly dashboard and click [Create flag](https://app.launchdarkly.com/default/test/features/new), this will open a tab for configurations for the flag. 
![Create Service](/images/setup/create-flag-1.png)

1. Name the feature flag `upperimage` (which will also populate the Key with the `upperimage` value). Provide a description, and check the box for "SDKs using Client-side ID". The rest of the page can be optionally filled out. Once you've completed, select **"Save flag"** on the bottom.
![Image Flag](/images/setup/image-target-1.png)

1. Within the feature flag configuration screen, select **"Add user targets"**, and for the true variation select the drop down arrow and type in your username. Select **"Add User"**. 
![Add user target](/images/setup/user-target-1.png)
 

1. Scroll down to the **"Default rule"** section and set SERVE to **"False"**. This will ensure that all users accessing the application by default have the feature disabled. 
![Set default rule](/images/setup/user-target-2.png)

1. Return to the top of the page and enable your feature flag, and select **"Review and save"**, confirm and accept your changes. 
![Enable targeting](/images/setup/user-target-3-enable.gif)

1. Return to our demo application and enter your **"username"** into the **"login box"** and select **"submit"**. You should see the LaunchDarkly Osmo logo display on the screen. This dark launch is only visible to the user you configured, and does not render for any of the other users who access the application. 
![Targeting Demo](/images/setup/targeting-demo.gif)