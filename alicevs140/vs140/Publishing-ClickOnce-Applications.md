---
title: "Publishing ClickOnce Applications"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-deployment
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eb6dfe79-f54c-4331-8e36-073688e70973
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Publishing ClickOnce Applications
When publishing a [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] application for the first time, publish properties can be set using the Publish Wizard. Only a few of the properties are available in the wizard; all other properties are set to their default values.  
  
 Subsequent changes to publish properties are made on the **Publish** page in the **Project Designer**.  
  
## Publish Wizard  
 You can use the Publish Wizard to set the basic settings for publishing your application. This includes the following publishing properties:  
  
-   Publishing Folder Location - where Visual Studio will copy the files (local computer, network file share, FTP server, or Web site)  
  
-   Installation Folder Location - where end users will install from (network file share, FTP server, Web site, CD/DVD)  
  
-   Online or Offline availability - if end users can access the application with or without a network connection  
  
-   Update frequency - how often the application checks for new updates.  
  
 For more information, see [How to: Publish a ClickOnce Application using the Publish Wizard](../vs140/How-to--Publish-a-ClickOnce-Application-using-the-Publish-Wizard.md).  
  
## Publish Page  
 The **Publish** page of the **Project Designer** is used to configure properties for ClickOnce deployment. The following table lists topics  
  
|Title|Description|  
|-----------|-----------------|  
|[How to: Specify Where Visual Studio Copies the Files](../vs140/How-to--Specify-Where-Visual-Studio-Copies-the-Files.md)|Describes how to set where Visual Studio puts the application files and manifests.|  
|[How to: Specify the Location Where End Users Will Install From](../vs140/How-to--Specify-the-Location-Where-End-Users-Will-Install-From.md)|Describes how to set the location where users go to download and install the application.|  
|[How to: Specify the ClickOnce Offline or Online Install Mode](../vs140/How-to--Specify-the-ClickOnce-Offline-or-Online-Install-Mode.md)|Describes how to set whether the application will be available offline or online.|  
|[How to: Set the ClickOnce Publish Version](../vs140/How-to--Set-the-ClickOnce-Publish-Version.md)|Describes how to set the ClickOnce **Publish Version** property, which determines whether or not the application that you are publishing will be treated as an update.|  
|[How to: Automatically Increment the ClickOnce Publish Version](../vs140/How-to--Automatically-Increment-the-ClickOnce-Publish-Version.md)|Describes how to automatically increment the Revision number of the **PublishVersion** each time you publish the application.|  
  
 For more information, see [Publish Page, Project Designer](../Topic/Publish%20Page,%20Project%20Designer.md)  
  
### Application Files Dialog Box  
 This dialog box allows you to specify how the files in your project are categorized for publishing, dynamic downloading, and updating. It contains a grid that lists the project files that are not excluded by default, or that have a download group.  
  
 To exclude files, mark files as data files or prerequisites, and create groups of files for conditional installation in the Visual Studio UI, see [How to: Specify Which Files Are Published via ClickOnce](../vs140/How-to--Specify-Which-Files-Are-Published-by-ClickOnce.md). You can also mark data files by using the Mage.exe. For more information, see [How to: Include a Data File in a ClickOnce Application](../vs140/How-to--Include-a-Data-File-in-a-ClickOnce-Application.md).  
  
### Prerequisites Dialog Box  
 This dialog box specifies which prerequisite components are installed, as well as how they are installed. For more information, see [How to: Install Prerequisites with a ClickOnce Application](../vs140/How-to--Install-Prerequisites-with-a-ClickOnce-Application.md) and [Prerequisites Dialog Box](../Topic/Prerequisites%20Dialog%20Box.md).  
  
### Application Updates Dialog Box  
 This dialog box specifies how the application installation should check for updates. For more information, see [How to: Manage Updates for a ClickOnce Application](../Topic/How%20to:%20Manage%20Updates%20for%20a%20ClickOnce%20Application.md).  
  
### Publish Options Dialog Box  
 The Publish Options dialog box specifies an application's deployment options.  
  
|||  
|-|-|  
|[How to: Change the Publish Language for a ClickOnce Application](../vs140/How-to--Change-the-Publish-Language-for-a-ClickOnce-Application.md)|Describes how to specify a language and culture to match the localized version.|  
|[How to: Specify a Start Menu Name for a ClickOnce Application](../vs140/How-to--Specify-a-Start-Menu-Name-for-a-ClickOnce-Application.md)|Describes how to change the display name for a ClickOnce application.|  
|[How to: Specify a Link for Technical Support](../vs140/How-to--Specify-a-Link-for-Technical-Support.md)|Describes how to set the **Support URL** property, which identifies a Web page or file share where users can go to get information about the application.|  
|[How to: Specify a Support URL for Individual Prerequisites in a ClickOnce Deployment](../vs140/How-to--Specify-a-Support-URL-for-Individual-Prerequisites-in-a-ClickOnce-Deployment.md)|Demonstrated how to manually alter an application manifest to include individual support URLs for each prerequisite.|  
|[How to: Specify a Publish Page for a ClickOnce Application](../vs140/How-to--Specify-a-Publish-Page-for-a-ClickOnce-Application.md)|Describes how to generate and publish a default Web page (publish.htm) along with the application|  
|[How to: Customize the Default Web Page for a ClickOnce Application](../vs140/How-to--Customize-the-Default-Web-Page-for-a-ClickOnce-Application.md)|Describes how to customize the Web page that is automatically generated and published along with the application.|  
|[How to: Enable AutoStart for CD Installations](../vs140/How-to--Enable-AutoStart-for-CD-Installations.md)|Describes how to enable AutoStart so that the ClickOnce application is automatically launched when the media is inserted.|  
  
## Related Topics  
  
|Title|Description|  
|-----------|-----------------|  
|[How to: Create File Associations For a ClickOnce Application](../vs140/How-to--Create-File-Associations-For-a-ClickOnce-Application.md)|Describes how to add file name extension support to a ClickOnce application.|  
|[How to: Retrieve Query String Information in a ClickOnce Application](../Topic/How%20to:%20Retrieve%20Query%20String%20Information%20in%20an%20Online%20ClickOnce%20Application.md)|Demonstrates how to retrieve parameters passed in the URL used to run a ClickOnce application.|  
|[How to: Disable URL Activation of ClickOnce Applications by Using the Designer](../vs140/How-to--Disable-URL-Activation-of-ClickOnce-Applications-by-Using-the-Designer.md)|Describes how to force users to start the application from the **Start** menu by using the designer.|  
|[How to: Disable URL Activation of ClickOnce Applications](../vs140/How-to--Disable-URL-Activation-of-ClickOnce-Applications.md)|Describes how to force users to start the application from the **Start** menu.|  
|[Walkthrough: Downloading Assemblies on Demand with the ClickOnce Deployment API Using the Designer](../Topic/Walkthrough:%20Downloading%20Assemblies%20on%20Demand%20with%20the%20ClickOnce%20Deployment%20API%20Using%20the%20Designer.md)|Explains how to download application assemblies only when they are first used by the application using the designer.|  
|[Walkthrough: Downloading Assemblies on Demand with the ClickOnce Deployment API](../Topic/Walkthrough:%20Downloading%20Assemblies%20on%20Demand%20with%20the%20ClickOnce%20Deployment%20API.md)|Explains how to download application assemblies only when they are first used by the application.|  
|[Walkthrough: Downloading Satellite Assemblies on Demand with the ClickOnce Deployment API](../Topic/Walkthrough:%20Downloading%20Satellite%20Assemblies%20on%20Demand%20with%20the%20ClickOnce%20Deployment%20API.md)|Describes how to mark your satellite assemblies as optional, and download only the assembly a client machine needs for its current culture settings.|  
|[Walkthrough: Manually Deploying a ClickOnce Application](../Topic/Walkthrough:%20Manually%20Deploying%20a%20ClickOnce%20Application.md)|Explains how to use .NET Framework utilities to deploy your ClickOnce application.|  
|[Walkthrough: Manually Deploying a ClickOnce Application that Does Not Require Re-Signing and that Preserves Branding Information](../vs140/Walkthrough--Manually-Deploying-a-ClickOnce-Application-that-Does-Not-Require-Re-Signing-and-that-Preserves-Branding-Information.md)|Explains how to use .NET Framework utilities to deploy your ClickOnce application without re-signing the manifests.|  
|[NIB: How to: Optimize an Application for a Specific CPU Type](assetId:///294a75d2-4279-4b72-8298-2bea05be907a)|Explains how to publish for a 64-bit processor by changing the **Target CPU** or **Platform target** property in your project.|  
|[Walkthrough: Enabling a ClickOnce Application to Run on Multiple .NET Framework Versions](assetId:///7f4383af-ed87-4853-b4d4-02a3967a5fd9)|Explains how to enable a ClickOnce application to install and run on multiple versions of the NET Framework.|  
|[Walkthrough: Creating a Custom Installer for a ClickOnce Application](../Topic/Walkthrough:%20Creating%20a%20Custom%20Installer%20for%20a%20ClickOnce%20Application.md)|Explains how to create a custom installer to install a ClickOnce application.|  
|[How to: Publish a WPF Application with Visual Styles Enabled](../vs140/How-to--Publish-a-WPF-Application-with-Visual-Styles-Enabled.md)|Provides step-by-step instructions to resolve an error that appears when you attempt to publish a WPF application that has visual styles enabled.|  
  
## See Also  
 [ClickOnce Security and Deployment](../Topic/ClickOnce%20Security%20and%20Deployment.md)   
 [ClickOnce Reference](../Topic/ClickOnce%20Reference.md)