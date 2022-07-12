---
title: "LaunchDarkly Account Setup"
chapter: true
weight: 11
---

## Create a LaunchDarkly account

LaunchDarkly provides a 14-day trial for users to explore LaunchDarkly capabilities. To execute the tasks within this workshop, you'll need to create a LaunchDarkly account. 

1 . Sign up for a free LaunchDarkly account through the AWS Marketplace [page](https://aws.amazon.com/marketplace/pp/prodview-x22m6p4lybzwe?trk=el_a134p000003yrYeAAI&trkCampaign=AWSMP_pdp_dev_x_dg&sc_channel=el&sc_campaign=el_awsmp_mult&sc_outcome=Marketplace)


<img src=/images/setup/ld-aws-marketplace.png>

After creating your LaunchDarkly account and logging in, you'll be placed in your default project.

2 . Navigate to the [Account settings/Projects tab/AWS](https://app.launchdarkly.com/settings/projects/default/environments) and copy the **client-side ID** for the Test environment (juts click on it!)

<img src=/images/setup/ld_client_id.png>
{{% notice info %}}
The Client-side ID will be used as a part of the App Runner configuration in the next step
{{% /notice %}}

<table class="credit">
<tr class="credit"><td class="credit" style="width:100%">
{{% notice note %}}
The SDK keys on this page enable the [LaunchDarkly SDKs](https://docs.launchdarkly.com/sdk) to communicate back with the LaunchDarkly service. Integrating these SDKs allows your application to pull down feature flags values from the globally distributed Flag Delivery Network.
{{% /notice %}}
</td></tr>
</table>
