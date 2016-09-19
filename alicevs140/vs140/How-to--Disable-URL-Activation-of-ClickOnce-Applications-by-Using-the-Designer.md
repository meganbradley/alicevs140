---
title: "How to: Disable URL Activation of ClickOnce Applications by Using the Designer"
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
ms.assetid: a337a582-e67c-409a-b52e-607cd1a8fc57
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Disable URL Activation of ClickOnce Applications by Using the Designer
Typically, a [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] application will start automatically immediately after it is installed from a Web server. For security reasons, you may decide to disable this behavior, and tell users to start the application from the **Start** menu instead. The following procedure describes how to disable URL activation.  
  
 This technique can be used only for [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] applications installed on the user's computer from a Web server. It cannot be used for online-only applications, which can be started only by using their URL. For more information about the difference between online-only and installed applications, see [Choosing a ClickOnce Deployment Strategy](../vs140/Choosing-a-ClickOnce-Deployment-Strategy.md).  
  
 This procedure uses [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. You can also accomplish this task by using the [!INCLUDE[winsdklong](../vs140/includes/winsdklong_md.md)]. For more information, see [How to: Disable URL Activation of ClickOnce Applications](../vs140/How-to--Disable-URL-Activation-of-ClickOnce-Applications.md).  
  
## Procedure  
  
#### To disable URL activation for your application  
  
1.  Right-click your project name in **Solution Explorer**, and click **Properties**.  
  
2.  On the **Properties** page, click the **Publish** tab.  
  
3.  Click **Options**.  
  
4.  Click **Manifests**.  
  
5.  Select the check box labeled **Block application from being activated via a URL**.  
  
6.  Deploy your application.  
  
## See Also  
 [Publishing ClickOnce Applications](../vs140/Publishing-ClickOnce-Applications.md)