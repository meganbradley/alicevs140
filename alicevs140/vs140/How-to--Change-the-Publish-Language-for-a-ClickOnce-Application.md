---
title: "How to: Change the Publish Language for a ClickOnce Application"
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
ms.assetid: ef5024c4-cda1-4970-bc75-32a2a10c92c3
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Change the Publish Language for a ClickOnce Application
When publishing a [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] application, the user interface displayed during installation defaults to the language and culture of your development computer. If you are publishing a localized application, you will need to specify a language and culture to match the localized version. This is determined by the `Publish language` property for your project.  
  
 The `Publish language` property can be set in the **Publish Options** dialog box, accessible from the **Publish** page of the **Project Designer**.  
  
> [!NOTE]
>  The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition. To change your settings, choose **Import and Export Settings** on the **Tools** menu. For more information, see [Customizing Development Settings in Visual Studio](assetId:///22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
### To change the publish language  
  
1.  With a project selected in **Solution Explorer**, on the **Project** menu, click **Properties**.  
  
2.  Click the **Publish** tab.  
  
3.  Click the **Options** button to open the **Publish Options** dialog box.  
  
4.  Click **Description**.  
  
5.  In the **Publish Options** dialog box, select a language and culture from the **Publish language** drop-down list, and then click **OK**.  
  
## See Also  
 [Publishing ClickOnce Applications](../vs140/Publishing-ClickOnce-Applications.md)   
 [How to: Publish a ClickOnce Application](../vs140/How-to--Publish-a-ClickOnce-Application-using-the-Publish-Wizard.md)