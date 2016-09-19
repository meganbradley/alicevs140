---
title: "How to: Specify Where Visual Studio Copies the Files"
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
ms.assetid: 6c552700-dda3-49fe-af98-4717344fda07
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Specify Where Visual Studio Copies the Files
When you publish an application by using ClickOnce, the `Publish Location` property specifies the location where the application files and manifest are put. This can be a file path or the path to an FTP server.  
  
 You can specify the `Publish Location` property on the **Publish** page of the **Project Designer**, or by using the Publish Wizard. For more information, see [How to: Publish a ClickOnce Application](../vs140/How-to--Publish-a-ClickOnce-Application-using-the-Publish-Wizard.md).  
  
> [!NOTE]
>  When you install more than one version of an application by using ClickOnce, the installation moves earlier versions of the application into a folder named Archive, in the publish location that you specify. Archiving earlier versions in this manner keeps the installation directory clear of folders from the earlier version.  
  
### To specify a publishing location  
  
1.  With a project selected in **Solution Explorer**, on the **Project** menu, click **Properties**.  
  
2.  Click the **Publish** tab.  
  
3.  In the **Publish Location** field, enter the publishing location by using one of the following formats:  
  
    -   To publish to a file share or disk path, enter the path by using either a UNC path (\\\Server\ApplicationName) or a file path (C:\Deploy\ApplicationName).  
  
    -   To publish to an FTP server, enter the path using the format ftp://ftp.microsoft.com/ApplicationName.  
  
     Note that text must be present in the **Publishing Location** box in order for the Browse (**...**) button to work.  
  
## See Also  
 [Publishing ClickOnce Applications](../vs140/Publishing-ClickOnce-Applications.md)   
 [How to: Publish a ClickOnce Application](../vs140/How-to--Publish-a-ClickOnce-Application-using-the-Publish-Wizard.md)