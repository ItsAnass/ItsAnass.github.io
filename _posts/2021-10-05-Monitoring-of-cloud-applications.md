---
title: "Monitoring of cloud applications."
layout: post
---
Describe the application, what does it do?

I used a previous application which was created in lesson 6 which was an  ASP.NET Web App where we can save names to my Azure Storage(locally).









I needed to download ("Microsoft.ApplicationInsights.AspNetCore") Nuget package and then I created Application Insight to my app service and I connected them using the InstrumentationKey and I added the configure Log Levels to my appsettings file which looks like this:

![JSFile](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Logging/Screenshot%202021-10-05%20180243.png?raw=true)

I then enabled Application Insights in the ConfigureServices method of the Startup class by adding:
services.AddApplicationInsightsTelemetry();
which looks like this:

![JSFile](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Logging/Screenshot%202021-10-05%20181044.png?raw=true)

I added also "@Html.Raw(JavaScriptSnippet.FullScript)" To my _Layout file which looks like this:

![JSFile](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Logging/121212.png?raw=true)

This will evaluate if Telemetry has been disabled in the config and if the instrumentation key was provided by either setting InstrumentationKey or ConnectionString.

I then added "@inject Microsoft.ApplicationInsights.AspNetCore.JavaScriptSnippet JavaScriptSnippet" To my _ViewImports file which helps to inject Application Insights JavaScript into application code which looks like this:

![JSFile](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Logging/Screenshot%202021-10-05%20183625.png?raw=true)

## Explain your queries?

![JSFile](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Logging/Screenshot%202021-10-05%20183433.png?raw=true)

Calculates the duration of the operations this is important to improve the responsiveness, throughput, quality, cost, and efficiency of production or service systems.


![JSFile](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Logging/Screenshot%202021-10-05%20183554.png?raw=true)

It shows a chart which contains the amount of requests from the top 10 countries using the website.


## Resources

[Implement logging in a .NET](https://docs.microsoft.com/en-us/learn/modules/aspnet-logging/)

[The Kusto Query Language](https://azure-training.com/azure-data-science/the-kusto-query-language/)














