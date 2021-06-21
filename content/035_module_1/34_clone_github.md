---
title: "3. Workspace Set up"
chapter: true
weight: 14
---

## Fork the source repository

Fork this [GitHub repository](https://github.com/launchdarkly-labs/ld-aws-workshop-module1-app), this repo contains the application which will be used by App Runner as the source code repository (AWS Connector is used here).


## Create a LaunchDarkly account

1 . Sign up for a free LaunchDarkly account through the AWS market place [page](https://aws.amazon.com/marketplace/pp/prodview-x22m6p4lybzwe)

<img src=/images/setup/ld-aws-marketplace.png>

2 . Navigate to the [Account settings/Projects tab](https://app.launchdarkly.com/settings/projects) and copy the **client-side ID** for the Production environment -- this will be used as a part of the App Runner configuration
<img src=/images/setup/ld_client_id.png>
{{% notice info %}}
The Client-side ID will be used as a part of the App Runner configuration in the next step
{{% /notice %}}
