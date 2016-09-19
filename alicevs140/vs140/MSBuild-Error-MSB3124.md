---
title: "MSBuild Error MSB3124"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d8365103-aa9d-400e-9c24-0a43e2bfbd14
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3124
**MSB3124: A file association has already been created for extension '<extensionname\>'.**  
  
 This error occurs when a duplicate file association extension is encountered.  
  
### To correct this error  
  
-   Remove [<fileAssociation\> Element](../vs140/ClickOnce-Deployment-Manifest.md)`extension` attributes that are not unique. Each listed <fileAssociation\> element's extension attributes must be unique.  
  
## See Also  
 [Publish Page, Project Designer](../Topic/Publish%20Page,%20Project%20Designer.md)   
 [ClickOnce Application Manifest](../vs140/ClickOnce-Application-Manifest.md)