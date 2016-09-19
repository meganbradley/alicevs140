---
title: "Build cross-platform apps with Visual Studio Tools for Apache Cordova"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 34d3c1be-22b3-4812-97fb-10b4e8ad2134
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Build cross-platform apps with Visual Studio Tools for Apache Cordova
[!INCLUDE[cordova_header](../vs140/includes/cordova_header_md.md)]  
  
 You can build cross-platform apps for iOS, Android, and Windows devices by using Visual Studio Tools for Apache Cordova. The easy-to-use installer identifies and installs the right versions of the required SDKs, tools, and libraries that you need to build [Apache Cordova](http://cordova.apache.org/) apps. Use the Visual Studio debugger to attach to iOS, Android, and Windows apps, hit breakpoints, and inspect code using the console and DOM Explorer. Apache Cordova enables cross-platform development standard web technologies such as HTML, CSS, and JavaScript.  
  
 You can build apps using the tools for these devices and platforms:  
  
-   Android 2.3.3 and later (4.4 provides the best developer experience)  
  
-   iOS 6, 7, and 8  
  
-   Windows 8 and 8.1  
  
-   Windows Phone 8 and 8.1  
  
> [!NOTE]
>  Visual Studio Tools for Apache Cordova has been tested for use with Cordova 5.1.1 and 4.3.1. You can select a different version using the [configuration designer](../Topic/Configure%20Your%20App%20Built%20with%20Visual%20Studio%20Tools%20for%20Apache%20Cordova.md). However, using an untested version may result in unexpected behaviors.  
  
 When you develop apps using Visual Studio Tools for Apache Cordova, Visual Studio provides these benefits:  
  
-   **Easy installation.** Manual installation of Cordova involves a lot of work to find, install, and maintain the correct version of all the third-party software required to support native platforms. Our third-party installer handles all of that for you and gets you up and running quickly.  
  
-   **Plugin management.** Cordova plugins provide access to native APIs using a JavaScript interface. Support for custom plugins like those that turn a mobile phone into a barcode scanner can help you provide rich experiences within your app. Visual Studio and IntelliSense make it easy to add and work with custom plugins and core plugins as well.  
  
-   **Unified debugging experience.** Cross-platform development often requires a different tool for debugging each device, emulator, or simulator. Different tools mean different workflows and lost productivity every time you switch devices. With Visual Studio, you can use the same world-class debugging tools for all deployment targets, including iOS devices and emulators, Android devices and emulators, Windows, and the Apache Ripple emulator.  
  
-   **Write once, deploy everywhere.** The common JavaScript and plugin APIs in Cordova make it easy to write an app using a single code base that deploys to all target platforms—iOS, Android, and Windows. Of course, you can always write platform-specific code if and when you need it.  
  
-   **Command line interoperability.** Visual Studio solutions directly reflect the file system and are updated in real time; this means that you can use any command line tool.  
  
-   **Multi-Version Cordova support.** Visual Studio solutions allow you to easily change to different versions of Cordova in your project.  
  
##  <a name="GetTools"></a> Get the tools  
 [Download Visual Studio 2015](http://aka.ms/mchm38) and select a custom installation with Cross Platform Mobile Development > HTML/JavaScript selected. You must also install the [remotebuild](https://www.npmjs.com/package/remotebuild) agent on OSX for iOS support.  
  
 For installation instructions, see [Install Visual Studio Tools for Apache Cordova](../vs140/Install-Visual-Studio-Tools-for-Apache-Cordova.md), and to get started writing your first app, see [Create your first app](../vs140/Create-Your-First-App-Using-Visual-Studio-Tools-for-Apache-Cordova.md).  
  
## Download a sample  
 The ToDoList sample app shows how you can use different frameworks for your Cordova app. ToDoList allows users to create new tasks, check them off, and remove them. The app uses Microsoft Azure Mobile Services to store data, and also uses Bing Maps to provide valid addresses.  
  
-   [AngularJS sample](http://go.microsoft.com/fwlink/p/?LinkID=398516)  
  
-   [WinJS sample](http://go.microsoft.com/fwlink/p/?LinkID=398518)  
  
-   [Backbone sample](http://go.microsoft.com/fwlink/p/?LinkID=398517)  
  
 To download the ToDoList sample app for Visual Studio 2013, see the deprecated samples on GitHub.  
  
> [!TIP]
>  To download other samples for Visual Studio Tools for Apache Cordova that demonstrate multi-page navigation and other features, see the [Ionic SideMenu starter template](http://go.microsoft.com/fwlink/p/?LinkID=544745) and [WinJS Navigation template](http://go.microsoft.com/fwlink/p/?LinkID=544743) samples.  
  
## Get started  
  
-   [Install Visual Studio Tools for Apache Cordova](../vs140/Install-Visual-Studio-Tools-for-Apache-Cordova.md)   
     [Configure the tools](../vs140/Configure-the-Visual-Studio-Tools-for-Apache-Cordova.md)  
  
-   [Create your first app](../vs140/Create-Your-First-App-Using-Visual-Studio-Tools-for-Apache-Cordova.md)  
  
-   [Configure your app](../Topic/Configure%20Your%20App%20Built%20with%20Visual%20Studio%20Tools%20for%20Apache%20Cordova.md)  
  
-   [Manage plugins](../vs140/Manage-Plugins-for-Apps-Built-with-Visual-Studio-Tools-for-Apache-Cordova.md)  
  
-   [Deploy and run your app on different platforms](../Topic/Deploy%20and%20Run%20Your%20App%20Built%20with%20Visual%20Studio%20Tools%20for%20Apache%20Cordova.md):   
     [Run your app on Android](../vs140/Run-Your-Apache-Cordova-App-on-Android.md)  
     [Run your app on iOS](../vs140/Run-Your-Apache-Cordova-App-on-iOS.md)  
     [Run your app on Windows](../vs140/Run-Your-Apache-Cordova-App-on-Windows.md)  
     [Run your app on Windows Phone](../vs140/Run-Your-Apache-Cordova-App-on-Windows-Phone.md)  
     [Run your app on the Apache Ripple Emulator](../vs140/Run-Your-Apache-Cordova-App-on-the-Apache-Ripple-Simulator.md)  
  
-   [Debug your app](../Topic/Debug%20Your%20App%20Built%20with%20Visual%20Studio%20Tools%20for%20Apache%20Cordova.md)  
  
-   [Add Connected Services](../Topic/Add%20Connected%20Services%20to%20App%20Built%20with%20Visual%20Studio%20Tools%20for%20Apache%20Cordova.md)  
  
-   [Package your app](../vs140/Package-Your-App-Built-with-Visual-Studio-Tools-for-Apache-Cordova.md)  
  
-   [Publish your app](../Topic/Publish%20Your%20App%20Built%20with%20Visual%20Studio%20Tools%20for%20Apache%20Cordova.md)  
  
-   [Access a native Cordova Project](../Topic/Access%20a%20Native%20Cordova%20Project.md)  
  
-   [Samples, Tutorials, and Videos](../Topic/Samples,%20Tutorials,%20and%20Videos%20for%20Visual%20Studio%20Tools%20for%20Apache%20Cordova.md)   
     [Using Apache Cordova 5](http://go.microsoft.com/fwlink/p/?LinkID=618470) (github)   
     [An introduction to Cordova 5 security](http://go.microsoft.com/fwlink/p/?LinkID=617521) (github)   
     [Using Gulp with your Cordova projects](http://go.microsoft.com/fwlink/p/?LinkID=533767) (github)  
     [Building Cordova apps in a team / continuous integration environment](http://go.microsoft.com/fwlink/p/?LinkID=533743) (github)   
     [Package and publish your Cordova applications](https://github.com/Microsoft/cordova-docs/blob/master/tutorial-package-publish) (github)   
     [Build and Simulate iOS in the Cloud](../vs140/Build-and-Simulate-iOS-in-the-Cloud.md)  
     [Build a Cordova App for iOS using Parallels](../vs140/Build-a-Cordova-app-for-iOS-using-Parallels.md)  
     [Run the Android Emulator on OSX using Parallels](assetId:///0e904536-fd5e-4f44-bbeb-c1b2beb90e22)  
     [Create a Cordova App using O365 Discovery Service and the Files API](../vs140/Cordova-Sample-App-with-O365-Discovery-Service-and-the-Files-API.md)  
     [Create a Cordova App using O365 Outlook Services and Ionic](assetId:///8588f879-e841-496c-b289-dd6625949964)  
     [Convert a Cordova Project to a PhoneGap Project](../vs140/Convert-a-Cordova-Project-to-a-PhoneGap-Project.md)  
     [Tips, Tricks, and Workarounds](http://go.microsoft.com/fwlink/p/?LinkID=618469) (github)   
     [Known Issues](http://go.microsoft.com/fwlink/p/?LinkID=618471) (github)   
     [Video Walkthrough: Interoperability with Third-party Tools](../vs140/Video-Walkthrough--Interoperate-with-Third-Party-Tools.md)  
     [Video Walkthrough: Visual Studio Diagnostic Tools for Cordova](../vs140/Video-Walkthrough--Debug-using-Visual-Studio-Diagnostic-Tools-for-Cordova.md)  
  
-   [Community: Connect with Developers](../Topic/Community:%20Connect%20with%20Apache%20Cordova%20Developers.md)  
  
 ![Download the tools](../vs140/media/Cordova_Install_Download.png "Cordova_Install_Download") [Get the Visual Studio Tools for Apache Cordova](http://aka.ms/mchm38) or [learn more](https://www.visualstudio.com/cordova-vs.aspx)  
  
## See Also  
 [Visual Studio Tools for Apache Cordova download](http://aka.ms/mchm38)   
 [Visual Studio Tools for Apache Cordova FAQ](http://go.microsoft.com/fwlink/p/?linkid=398476)   
 [Known Issues](http://go.microsoft.com/fwlink/p/?linkid=398782)   
 [Cordova Build process in Visual Studio](../Topic/Deploy%20and%20Run%20Your%20App%20Built%20with%20Visual%20Studio%20Tools%20for%20Apache%20Cordova.md#BuildProcess)