---
title: "How to: Disable URL Activation of ClickOnce Applications"
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
ms.assetid: db31a16b-960f-4264-91d7-c7c40f876068
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Disable URL Activation of ClickOnce Applications
Typically, a [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] application will launch automatically immediately after it is installed from a Web server. For security reasons, you may decide to disable this behavior, and tell users to launch the application from the **Start** menu instead. The following procedure describes how to disable URL activation.  
  
 This technique can be used only for [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] applications installed on the user's computer from a Web server. It cannot be used for online-only applications, which can be launched only by using their URL. For more information on the difference between online-only and installed applications, see [Choosing a ClickOnce Deployment Strategy](../vs140/Choosing-a-ClickOnce-Deployment-Strategy.md).  
  
 This procedure uses the [!INCLUDE[winsdklong](../vs140/includes/winsdklong_md.md)] tool MageUI.exe. For more information on this tool, see [Manifest Generation and Editing Tool, Graphical Client (MageUI.exe)](assetId:///f9e130a6-8117-49c4-839c-c988f641dc14). You can also perform this procedure using [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
## Procedure  
  
#### To disable URL activation for your application  
  
1.  Open your deployment manifest in MageUI.exe. If you have not yet created one, follow the steps in [Walkthrough: Deploying a ClickOnce Application Manually](../Topic/Walkthrough:%20Manually%20Deploying%20a%20ClickOnce%20Application.md).  
  
2.  Select the **Deployment Options** tab.  
  
3.  Clear the **Automatically run application after installing** check box.  
  
4.  Save and sign the manifest.  
  
## See Also  
 [Publishing ClickOnce Applications](../vs140/Publishing-ClickOnce-Applications.md)