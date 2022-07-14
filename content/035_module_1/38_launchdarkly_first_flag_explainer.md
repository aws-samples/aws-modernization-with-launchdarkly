---
title: "Understanding Feature Flags"
chapter: true
weight: 16
---

## Understanding Feature Flags


In order to leverage LaunchDarkly, we need to configure Feature Flags that can be toggled on or off. One half of this configuration lives within your application code, and the other half lives within the LaunchDarkly platform. In the following section, we will create our first feature flag in LaunchDarkly. 

There are a number of different types of feature flags that can be created with LaunchDarkly. 

- **Boolean** flags allow you to evaluate true vs false. 
- **String** flags allow us to pass text based content into an area based on targeting data. 
- **Number** flags allow us to pass numeric values in as feature flags. Finally, 
- **JSON** based flags allow us to create blocks of JSON (JavaScript object notation) objects and pass them into the application, these types of flags are useful for passing sets of configuration details through to your application.

Beyond the type of flags that can be created, we can also create **flag prerequisites** between different feature flags that allow you to ensure flags are only being enabled when supporting configurations are in place. 

We can also use **individual targets** and **targeting rules** to control which user cohorts are receicing a set of flag configurations. We'll explore this more later in the workshop! 

For now, lets create our first feature flag!