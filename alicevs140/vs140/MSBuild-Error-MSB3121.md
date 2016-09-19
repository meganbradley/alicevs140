---
title: "MSBuild Error MSB3121"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c1e83a2a-515f-412d-b8b7-4821e510a923
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3121
**MSB3121: The file association element in the application manifest is missing one or more of the following required attributes: extension, description, progid, or default icon.**  
  
 The [<fileAssociation\> Element](../vs140/ClickOnce-Deployment-Manifest.md) must contain values for all four attributes.  
  
### To correct this error  
  
-   Set each [<fileAssociation\> Element](../vs140/ClickOnce-Deployment-Manifest.md) attribute to a valid value.  
  
## See Also  
 [Publish Page, Project Designer](../Topic/Publish%20Page,%20Project%20Designer.md)   
 [ClickOnce Application Manifest](../vs140/ClickOnce-Application-Manifest.md)