---
title: "How to: Specify the ClickOnce Offline or Online Install Mode"
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
ms.assetid: 0aee5fc1-e966-4bda-9b8f-d9997aeaa779
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Specify the ClickOnce Offline or Online Install Mode
The `Install Mode` for a [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] application determines whether the application will be available offline or online. When you choose **The application is available online only**, the user must have access to the [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] publishing location (either a Web page or a file share) in order to run the application. When you choose **The application is available offline as well**, the application adds entries to the **Start** menu and the **Add or Remove Programs** dialog box; the user is able to run the application when they are not connected.  
  
 The `Install Mode` can be set on the **Publish** page of the **Project Designer**.  
  
 **Note** The `Install Mode` can also be set using the Publish wizard. For more information, see [How to: Publish a ClickOnce Application](../vs140/How-to--Publish-a-ClickOnce-Application-using-the-Publish-Wizard.md).  
  
### To make a ClickOnce application available online only  
  
1.  With a project selected in **Solution Explorer**, on the **Project** menu, click **Properties**.  
  
2.  Click the **Publish** tab.  
  
3.  In the **Install Mode and Settings** area, click the **The application is available online only** option button.  
  
### To make a ClickOnce application available online or offline  
  
1.  With a project selected in **Solution Explorer**, on the **Project** menu, click **Properties**.  
  
2.  Click the **Publish** tab.  
  
3.  In the **Install Mode and Settings** area, click the **The application is available offline as well** option button.  
  
     When installed, the application adds entries to the **Start** menu and to **Add or Remove Programs** in Control Panel.  
  
## See Also  
 [Publishing ClickOnce Applications](../vs140/Publishing-ClickOnce-Applications.md)   
 [How to: Publish a ClickOnce Application](../vs140/How-to--Publish-a-ClickOnce-Application-using-the-Publish-Wizard.md)   
 [Choosing a ClickOnce Deployment Strategy](../vs140/Choosing-a-ClickOnce-Deployment-Strategy.md)