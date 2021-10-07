# dotnet-test-apps

## Blazor WebAssembly

Target: BlazorWebAssembly

### Script

1. Right click on the **BlazorWasm** csproj file
1. Click on **Publish to AWS**
1. If you are deploying for first time, select **New Target**.
    - If you want to redeploy on the existing deployment project, select **Existing target**. This will list recently deployed compatible projects. Select any. Skip next step because selected existing deployment recommendation has been selected automatically.
1. Select **Blazor WebAssembly App** recommendation.
    - It should be selected by default.
1. If you want change the deployment settings, click on **Edit publish settings**
1. If all settings look good, click on Publish.

## MvcWebApplication (ASP.NET Core MVC)

Target:  Amazon ECS using Fargate
### Script

1. Right click on the **MvcWebApplication** csproj file
1. Click on **Publish to AWS**
1. If you are deploying for first time, select **New Target**.
    - If you want to redeploy on the existing deployment project, select **Existing target**. This will list recently deployed compatible projects. Select any. Skip next step because selected existing deployment recommendation has been selected automatically.
1. Select **ASP.NET Core App to Amazon ECS using Fargate** recommendation.
    - It should be selected by default.
1. If you want change the deployment settings, click on **Edit publish settings**
    - Try changing VPC, Cluster or Task Count settings.
    - Explore advanced settings by checking **Show advanced settings**
1. If all settings look good, click on Publish.

Bonus: try to deploy **MvcWebApplication** to other recommendations.

## WeatherReactSpa (React + .NET Core WebAPI backend)

Target: Amazon Elastic Beanstalk on Linux

### Script

1. Right click on the **WeatherReactSpa** csproj file
1. Click on **Publish to AWS**
1. If you are deploying for first time, select **New Target**.
    - If you want to redeploy on the existing deployment project, select **Existing target**. This will list recently deployed compatible projects. Select any. Skip next step because selected existing deployment recommendation has been selected automatically.
1. Select **ASP.NET Core App to Amazon Elastic Beanstalk on Linux** recommendation.
    - It should be selected by default.
1. If you want change the deployment settings, click on **Edit publish settings**
    - Try changing Environment Type
    - Explore advanced settings by checking **Show advanced settings**
1. If all settings look good, click on Publish.

Bonus: try to deploy **WeatherReactSpa** to other recommendations.