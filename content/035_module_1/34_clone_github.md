---
title: "3. Workspace Set up"
chapter: true
weight: 14
---

## Fork the source repository

Fork this [GitHub repository](https://github.com/launchdarkly-labs/ld-aws-workshop-module1-app), this repo contains the application which will be used by App Runner as the source code repository (AWS Connector is used here).


## Create a LaunchDarkly account

1 . Access this [page](https://launchdarkly.com/start-trial/) and sign up for a free LaunchDarkly account

<img src=/images/setup/ld_trial.png>

2 . Navigate to the [Account settings/Projects tab](https://app.launchdarkly.com/settings/projects) and copy the **client-side ID** for the Production environment -- this will be used as a part of the App Runner configuration
<img src=/images/setup/ld_client_id.png>
{{% notice info %}}
The Client-side ID will be used as a part of the App Runner configuration in the next step
{{% /notice %}}
