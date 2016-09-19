---
title: "MSBuild Error MSB3125"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f8a08b05-1946-4788-8577-ceefde785e95
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3125
**MSB3125: The application is using file associations but has no EntryPoint build parameter.**  
  
 This error occurs when no entryPoint build parameter is present. When you configure an application to use file associations, there must be an entryPoint build parameter in the application manifest. The <entryPoint\> element identifies the assembly that should be executed when the application is run.  
  
### To correct this error  
  
-   Set the [<entryPoint\> Element](../Topic/%3CentryPoint%3E%20Element%20\(ClickOnce%20Application\).md) to a valid value. For more information, see [ClickOnce Application Manifest](../vs140/ClickOnce-Application-Manifest.md).  
  
## See Also  
 [Publish Page, Project Designer](../Topic/Publish%20Page,%20Project%20Designer.md)   
 [ClickOnce Application Manifest](../vs140/ClickOnce-Application-Manifest.md)