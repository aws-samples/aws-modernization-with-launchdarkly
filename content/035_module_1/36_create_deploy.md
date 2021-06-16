---
title: "4. Create and Deploy"
chapter: true
weight: 18
---

## Setting up the AWS App Runner Service

Open the AWS console, and browse to the AWS App Runner service, or [https://console.aws.amazon.com/apprunner/home](https://console.aws.amazon.com/apprunner/home):

![Create Service](/images/setup/service-create-service.png)

Select “Create a service”.

![Source Service](/images/setup/service-source.png)

For your Repository type, select “Source code repository”. This will require you to add a connection to GitHub in order for AWS App Runner to deploy your new service. Select “Add new”.

![Source Service](/images/setup/service-deployment1.png)

Underneath Deployment trigger, select “Automatic” in order to automatically redeploy your application whenever a code change is pushed to the main branch of your Github repository, then select “Next”.

![Source Service](/images/setup/service-deployment2.png)

For this example, we are going to specify all the settings for our service manually. This is in order to show the control that AWS App Runner gives you.

Select “Configure all settings here”, then underneath Runtime select “Python 3” from the dropdown.

Under Build commend, enter `pip install -r requirservice-ements.txt`.

Under Start command, enter `python app/server.py`.

Under Port, enter `8080`.

Select ‘Next’ to continue.

![Source Service](/images/setup/service-deployment3.png)

In this step we will give our new service a name - `my-aws-workshop-aa`. 

Under Environment variables, enter the Key as `CLIENT_ID`, and the vaule as the client-side ID from the LaunchDarkly.

Leave the rest of these settings as defaults.

Select “Next” to continue.

![Source Service](/images/setup/service-deployment4.png)

Finally, review your settings and select “Create & deploy”. This will take a few minutes.

![Source Service](/images/setup/service-creating.png)

Once status has moved to “Complete", you can click on the url listed below "Default domain" in order to view the actual web application you have just deployed.

Congratulations, you have just deployed a simple web service using App Runner!

![Source Service](/images/setup/demo-app.png)


{{% notice info %}}
This will take about 1-2 minutes to provision
{{% /notice %}}