---
title: "4. Create and Deploy"
chapter: true
weight: 18
---

AWS App Runner allows us to run web based applications directly on AWS without managing underlying infrastructure. Services can be deployed by simply connecting a Git repository or specifying a container to run. 

## Setting up the AWS App Runner Service

Open the AWS console, and browse to the AWS App Runner service, or [https://console.aws.amazon.com/apprunner/home](https://console.aws.amazon.com/apprunner/home) and select "Create an App Runner service".
![Create Service](/images/setup/service-create-service.png)

For your Repository type, select “Source code repository”. This will require you to add a connection to GitHub in order for AWS App Runner to deploy your new service. Select “Add new”.
![Source Service](/images/setup/source-service.png)

Underneath Deployment trigger, select “Automatic” in order to automatically redeploy your application whenever a code change is pushed to the main branch of your Github repository, then select “Next”.
![Source Service](/images/setup/deployment-settings.png)

For this example, we are going to specify all the settings for our service manually. This is in order to show the control that AWS App Runner gives you. Select “Configure all settings here”, then underneath Runtime select “Node 14” from the dropdown.

Under Build commend, enter `npm install`.

Under Start command, enter `npm run start`.

Under Port, enter `3000`.

Select ‘Next’ to continue.

![Source Service](/images/setup/configure-build.png)

In this step we will give our new service a name - `my-aws-workshop-app`.

Under Environment variables, enter the Key as `REACT_APP_LD_SDK_KEY`, and the value as the client-side ID from the LaunchDarkly.

Leave the rest of these settings as defaults.

Select “Next” to continue.
![Source Service](/images/setup/configure-service.png)

Finally, review your settings and select “Create & deploy”. This will take a few minutes.

![Source Service](/images/setup/service-deploying.png)

Once status has moved to “Complete", you can click on the url listed below "Default domain" in order to view the actual web application you have just deployed.

Congratulations, you have just deployed a simple web service using App Runner!

![Source Service](/images/setup/full-app-demo.png)


{{% notice info %}}
This will take about 1-2 minutes to provision
{{% /notice %}}
