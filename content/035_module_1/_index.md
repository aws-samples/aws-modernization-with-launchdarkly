---
title: "Module 1: Your First LaunchDarkly Feature Flag"
chapter: true
draft: false
weight: 4
---

# YOUR FIRST LAUNCHDARKLY FEATURE FLAG

### Welcome

In this workshop we will learn to perform a release of new features in our demo application, while its running live on [AWS App Runner](https://aws.amazon.com/apprunner/). Once we learn how to create and release features, we'll leverage user targeting to influence which users can consume additonal features. This method of software release is referred to as "dark launching" and it allows developers to release code to different user cohorts without changing their expereince or redeploying the application code. 

In our applicatiom, we'll use these feature flags to demonstrate delivering these new features reliably, quickly and safely.

![Source Service](/images/setup/banner.png)

In the next steps we'll step through deploying our demo application into AWS App runner. 

### Learning Objectives
- How to set up AWS App Runner and deploy an application
- How to use a feature flag to decouple release from deploy
- How to target specific features at different user configurations 

### Steps

- Cloning the Github source repository for this workshop
- Creating & Deploying the workshop application using App Runner
- Accessing the LaunchDarkly portal to create/control feature flags