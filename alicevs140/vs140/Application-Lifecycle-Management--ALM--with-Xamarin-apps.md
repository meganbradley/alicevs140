---
title: "Application Lifecycle Management (ALM) with Xamarin apps"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tgt-pltfrm-cross-plat
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ff978cc2-5a25-46d6-921b-e51adaa65992
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Application Lifecycle Management (ALM) with Xamarin apps
Xamarin enables you to build cross-platform mobile apps targeting Android, iOS, and Windows using C#, .NET, and Visual Studio. Xamarin allows a large portion of code to be shared between platforms, with only a small percentage needing to be platform-specific. For more information on Xamarin itself, see [Visual Studio and Xamarin](../vs140/Visual-Studio-and-Xamarin.md).  
  
 Developing apps for modern platforms involves many more activities than just writing code. These activities, referred to as DevOps (development + operations), span the app’s complete lifecycle and include planning and tracking work, designing and implementing code, managing a source code repository, running builds, managing continuous integrations and deployments, testing (including unit tests and UI tests), running various forms of diagnostics in both development and production environments, and monitoring app performance and user behaviors in real time through telemetry and analytics.  
  
 Visual Studio together with Visual Studio Team Services and Team Foundation Server provide a variety of DevOps capabilities, also referred to as Application Lifecycle Management or ALM. Many of these are wholly applicable to cross-platform projects.  
  
 This is especially true with Xamarin apps because they are built with C# and .NET, around which some ALM tools are built. Other tools, require tight integration with build and runtime environments. Because Xamarin apps run on non-Windows platforms and use the Mono implementation of .NET, Xamarin provides specialized tools for certain needs.  
  
 The tables below identifies which Visual Studio ALM features you can expect to work well with a Xamarin project, and which ones have limitations. Refer to the linked documentation for details on the features themselves.  
  
## Agile tools  
 Reference link: **[Agile tools](assetId:///52aa8bc9-fc7e-4fae-9946-2ab255ca7503)** (using Visual Studio Team Services or TFS, including Team Explorer Everywhere)  
  
 General Comment: all planning and tracking features are independent of project type and coding languages.  
  
|Feature|Supported with Xamarin|Additional Comments|  
|-------------|----------------------------|-------------------------|  
|Manage backlogs and sprints|Yes||  
|Work tracking|Yes||  
|Team room collaboration|Yes||  
|Kanban boards|Yes||  
|Report and visualize progress|Yes||  
  
## Modeling  
 Reference link: **[Analyze and model your architecture](../vs140/Analyze-and-model-your-architecture.md)**  
  
 Design features are independent of coding language, or work with .NET languages like C#. See [Modeling Diagram Tools](../vs140/Scenario--Change-your-design-using-visualization-and-modeling.md#ModelingDiagramsTools) for what aspects are related to code.  
  
|Feature|Supported with Xamarin|Additional Comments|  
|-------------|----------------------------|-------------------------|  
|Sequence diagrams|Yes||  
|Dependency graphs|Yes||  
|Call hierarchy|Yes||  
|Class designer|Yes||  
|Architecture explorer|Yes||  
|UML diagrams (use case, activity, class, component, sequence, and DSL)|Yes||  
|Layer diagrams|Yes||  
|Layer validation|Yes||  
  
## Code  
  
|Feature|Supported with Xamarin|Additional Comments|  
|-------------|----------------------------|-------------------------|  
|[Use Team Foundation Version Control](assetId:///1d629052-c65d-4c5d-81eb-eaa4413fe285) or Visual Studio Team Services|Yes||  
|[Getting started with Git in Team Services](assetId:///32f46ecd-1b03-4ef0-a9c4-8a120da2b03f)|Yes||  
|[Code analysis/Improve code quality (references, suggested changes, etc.)](../vs140/Improve-Code-Quality.md)|Yes||  
|[CodeLens](../vs140/Find-code-changes-and-other-history-with-CodeLens.md)|Yes|Except across platform-specific boundaries where the implementation isn’t resolved until run time.|  
|[Code maps](../vs140/Use-code-maps-to-debug-your-applications.md)|Yes||  
  
## Build  
 Reference link: **[Build the application](assetId:///a971b0f9-7c28-479d-a37b-8fd7e27ef692)**  
  
|Feature|Supported with Xamarin|Additional Comments|  
|-------------|----------------------------|-------------------------|  
|On-premises TFS server|Yes|Build machines must have Xamarin installed and can be linked to an OSX machine to build for iOS. See [Configuring TFS for Xamarin](http://developer.xamarin.com/guides/cross-platform/ci/configuring_tfs/) (Xamarin website)|  
|On-premises build server linked to Visual Studio Team Services|Yes|See [Scale out and administer your build and deployment system](assetId:///2d258a0a-f178-4e93-9da1-eba61151af3c) for instructions.|  
|Hosted controller service of Visual Studio Team Services|Yes|See [Build your Xamarin app](assetId:///933a828e-cbb7-44c2-bac0-1e1e9d78bfa0).|  
|Build definitions with pre- and post-scripts|Yes||  
|Continuous integration including gated check-ins|Yes|Gated check-ins for TFVC only as Git works on a pull-request model rather than check-ins.|  
  
## Testing  
 Reference link: **[Testing the application](assetId:///796b7d6d-ad45-4772-9719-55eaf5490dac)**  
  
|Feature|Supported with Xamarin|Additional Comments|  
|-------------|----------------------------|-------------------------|  
|Planning tests, creating test cases and organizing test suites|Yes||  
|Manual testing|Yes||  
|Test Manager (record and playback tests)|Yes|Windows devices and Android emulators only from Visual Studio. Recording for all devices is possible with [Xamarin Test Recorder](https://www.xamarin.com/test-cloud/recorder).|  
|Code coverage|n/a||  
|[Unit tests](../Topic/Unit%20Test%20Your%20Code.md)|Yes|For Windows and Android targets, the built-in MSTest tools can be used. To run unit tests on Windows, Android, and iOS, Xamarin recommends NUnit. See [Configuring TFS for Xamarin](http://developer.xamarin.com/guides/cross-platform/ci/configuring_tfs/) (Xamarin website).|  
|[Automated (Coded) UI tests](../Topic/Use%20UI%20Automation%20To%20Test%20Your%20Code.md)|Windows only|Visual Studio's UI test recorder is Windows only. For all platforms, see [Xamarin Test Recorder](https://www.xamarin.com/test-cloud/recorder).|  
  
## Improve code quality  
 Reference link: **[Improve code quality](../vs140/Improve-Code-Quality.md)**  
  
|Feature|Supported with Xamarin|Additional Comments|  
|-------------|----------------------------|-------------------------|  
|[Code quality analysis](../vs140/Analyzing-Managed-Code-Quality-by-Using-Code-Analysis.md)|Yes||  
|[Code clone detection](../vs140/Finding-Duplicate-Code-by-using-Code-Clone-Detection.md)|Yes||  
|[Code metrics](../vs140/Measuring-Complexity-and-Maintainability-of-Managed-Code.md)|Yes||  
|[Performance profiling](../vs140/Performance-Explorer.md)|No|Use the [Xamarin Profiler](http://developer.xamarin.com/guides/cross-platform/deployment,_testing,_and_metrics/) through Xamarin Studio instead. Note that the Xamarin Profiler is currently in preview and does not yet work for Windows targets.|  
|[.NET Framework memory analysis](../vs140/Analyze-.NET-Framework-memory-issues.md)|No|Visual Studio tools do not have hooks into the Mono framework for profiling.|  
  
## Release management  
 Reference link: **[Automate deployments with Release Management](https://msdn.microsoft.com/library/vs/alm/release/overview)**  
  
|Feature|Supported with Xamarin|Additional Comments|  
|-------------|----------------------------|-------------------------|  
|Manage release processes|Yes||  
|Deployment to servers for side-loading via scripts|Yes||  
|Upload to app store|Partial|Extensions are available that can automate this process for some app stores.  See [Extensions for Visual Studio Team Services](https://marketplace.visualstudio.com/VSTS); for example, the [extension for Google Play](https://marketplace.visualstudio.com/items?itemName=ms-vsclient.google-play).|  
  
## Monitor with HockeyApp  
 Reference link: **[Monitor with HockeyApp](https://www.hockeyapp.net/features/)**  
  
|Feature|Supported with Xamarin|Additional Comments|  
|-------------|----------------------------|-------------------------|  
|Crash analytics, telemetry, and beta distribution|Yes||