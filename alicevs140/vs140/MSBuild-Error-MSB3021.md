---
title: "MSBuild Error MSB3021"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8cb3a860-6916-4406-b5c7-b1106b44b92a
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3021
**Unable to copy file "'<file\>'" to file "'<file\>'". '<error\>'**  
  
 The `Copy` task cannot copy the specified file.  
  
### To correct this error  
  
-   Check to see if the target file is locked (in use) by another application. Be sure you have permission to read the source file and to write the target file to the target folder. If the destination file path is extremely long, you may need to copy to a different location.  
  
## See Also  
 [Copy Task](../Topic/Copy%20Task.md)   
 [MSBuild Tasks](../Topic/MSBuild%20Tasks.md)