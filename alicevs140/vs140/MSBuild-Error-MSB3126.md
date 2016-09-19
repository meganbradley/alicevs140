---
title: "MSBuild Error MSB3126"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0c92cbb6-9100-4433-8113-f2f3a1432243
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3126
**MSB3126: The application is using file associations but is not marked for installation. File associations cannot be used for applications that are not installed such as applications hosted in a web browser.**  
  
 This error occurs when an application is configured to use file associations but the application's install mode is set to online only. Because online only applications typically run in a browser, file associations are not available.  
  
### To correct this error  
  
-   Set the **Install Mode and Settings** to **The application is available offline as well (launchable from Start menu)**. For more information, see [How to: Specify the ClickOnce Install Mode](../vs140/How-to--Specify-the-ClickOnce-Offline-or-Online-Install-Mode.md).  
  
## See Also  
 [Publish Page, Project Designer](../Topic/Publish%20Page,%20Project%20Designer.md)   
 [ClickOnce Application Manifest](../vs140/ClickOnce-Application-Manifest.md)