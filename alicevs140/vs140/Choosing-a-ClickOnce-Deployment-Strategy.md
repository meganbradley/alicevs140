---
title: "Choosing a ClickOnce Deployment Strategy"
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
ms.assetid: 98bcab65-ab8b-4ed1-9adc-fdacf92b8106
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Choosing a ClickOnce Deployment Strategy
There are three different strategies for deploying a [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] application; the strategy that you choose depends primarily on the type of application that you are deploying. The three deployment strategies are as follows:  
  
-   Install from the Web or a Network Share  
  
-   Install from a CD  
  
-   Start the application from the Web or a Network Share  
  
    > [!NOTE]
    >  In addition to selecting a deployment strategy, you will also want to select a strategy for providing application updates. For more information, see [Choosing a ClickOnce Update Strategy](../Topic/Choosing%20a%20ClickOnce%20Update%20Strategy.md).  
  
## Install from the Web or a Network Share  
 When you use this strategy, your application is deployed to a Web server or a network file share. When an end user wants to install the application, he or she clicks an icon on a Web page or double-clicks an icon on the file share. The application is then downloaded, installed, and started on the end user's computer. Items are added to the **Start** menu and **Add or Remove Programs** in **Control Panel**.  
  
 Because this strategy depends on network connectivity, it works best for applications that will be deployed to users who have access to a local-area network or a high-speed Internet connection.  
  
 If you deploy the application from the Web, you can pass arguments into the application when it is activated using a URL. For more information, see [How to: Retrieve Query String Information in a ClickOnce Application](../Topic/How%20to:%20Retrieve%20Query%20String%20Information%20in%20an%20Online%20ClickOnce%20Application.md). You cannot pass arguments into an application that is activated by using any of the other methods described in this document.  
  
 To enable this deployment strategy in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], click **From the Web** or **From a UNC path or file share** on the **How Installed** page of the Publish Wizard.  
  
 This is the default deployment strategy.  
  
## Install from a CD  
 When you use this strategy, your application is deployed to removable media such as a CD-ROM or DVD. As with the previous option, when the user chooses to install the application, it is installed and started, and items are added to the **Start** menu and **Add or Remove Programs** in **Control Panel**.  
  
 This strategy works best for applications that will be deployed to users without persistent network connectivity or with low-bandwidth connections. Because the application is installed from removable media, no network connection is necessary for installation; however, network connectivity is still required for application updates.  
  
 To enable this deployment strategy in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], click **From a CD-ROM or DVD-ROM** on the **How Installed** page of the Publish Wizard.  
  
 To enable this deployment strategy manually, change the **deploymentProvider** tag in the deployment manifest. (In Visual Studio, this property is exposed as **Installation URL** on the **Publish** page of the Project Designer. In Mage.exe it is **Start Location**.)  
  
## Start the Application from the Web or a Network Share  
 This strategy is like the first, except the application behaves like a Web application. When the user clicks a link on a Web page (or double-clicks an icon on the file share), the application is started. When users close the application, it is no longer available on their local computer; nothing is added to the **Start** menu or **Add or Remove Programs** in **Control Panel**.  
  
> [!NOTE]
>  Technically, the application is downloaded and installed to an application cache on the local computer, just as a Web application is downloaded to the Web cache. As with the Web cache, the files are eventually scavenged from the application cache. However, the perception of the user is that the application is being run from the Web or file share.  
  
 This strategy works best for applications that are used infrequently—for example, an employee-benefits tool that is typically run only one time each year.  
  
 To enable this deployment strategy in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], click **Do not install the application** on the **Install or Run From Web** page of the Publish Wizard.  
  
 To enable this deployment strategy, manually, change the **install** tag in the deployment manifest. (Its value can be **true** or **false**. In Mage.exe, use the **Online Only** option in the **Application Type** list.)  
  
## Web Browser Support  
 Applications that target .NET Framework 3.5 can be installed using any browser.  
  
 Applications that target .NET Framework 2.0 require Internet Explorer.  
  
## See Also  
 [ClickOnce Security and Deployment](../Topic/ClickOnce%20Security%20and%20Deployment.md)   
 [Choosing a ClickOnce Update Strategy](../Topic/Choosing%20a%20ClickOnce%20Update%20Strategy.md)   
 [How to: Publish a ClickOnce Application using the Publish Wizard](../vs140/How-to--Publish-a-ClickOnce-Application-using-the-Publish-Wizard.md)   
 [Securing ClickOnce Applications](../vs140/Securing-ClickOnce-Applications.md)