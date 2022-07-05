---
title: "3. Workspace Set up"
chapter: true
weight: 14
---

## Fork the source repository

Fork this [GitHub repository](https://github.com/launchdarkly-labs/ld-aws-devops-workshop) by launching the link and selecting the "Fork" button on the top right corner of the repository. 

A "Fork" is a standalone copy of the existing repository, in your own Git environment, that you can modify independently of the original code. 

Developer teams will often fork a project repository, and create "Branches" (copies of the code separate from the "main" code base) to perform development work against. 

This repo contains the application which will be used by App Runner as the source code repository (AWS Connector is used here). 

<table class="credit">
<tr class="credit"><td class="credit" style="width:100%">
{{% notice note %}}
Did you know that you can explore the application code right from your browser window? Open the github repository and press the . (the period) key on your keyboard, an IDE (integrated developer experience) will launch and you will be able to explore the code for the application.
{{% /notice %}}
</td></tr>
</table>


## Create a LaunchDarkly account

LaunchDarkly provides a 14-day trial for users to explore LaunchDarkly capabilities. To execute the tasks within this workshop, you'll need to create a LaunchDarkly account. 

1 . Sign up for a free LaunchDarkly account through the AWS Marketplace [page](https://aws.amazon.com/marketplace/pp/prodview-x22m6p4lybzwe?trk=el_a134p000003yrYeAAI&trkCampaign=AWSMP_pdp_dev_x_dg&sc_channel=el&sc_campaign=el_awsmp_mult&sc_outcome=Marketplace)


<img src=/images/setup/ld-aws-marketplace.png>

After creating your LaunchDarkly account and logging in, you'll be placed in your default project.

2 . Navigate to the [Account settings/Projects tab](https://app.launchdarkly.com/settings/projects) and copy the **client-side ID** for the Test environment -- this will be used as a part of the App Runner configuration
<img src=/images/setup/ld_client_id.png>
{{% notice info %}}
The Client-side ID will be used as a part of the App Runner configuration in the next step
{{% /notice %}}

<table class="credit">
<tr class="credit"><td class="credit" style="width:100%">
{{% notice note %}}
The SDK keys on this page enable the LaunchDarkly SDKs to communicate back with the LaunchDarkly service. Integrating these SDKs allows your application to pull down feature flags values from the globally distributed Flag Delivery Network.
{{% /notice %}}
</td></tr>
</table>
