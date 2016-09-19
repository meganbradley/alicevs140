---
title: "Specified registry key is not valid because it contains two or more consecutive backslashes"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0d78b6f7-5759-45b4-8c37-c6902ada76ff
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Specified registry key is not valid because it contains two or more consecutive backslashes
A registry key specified with a path contains two or more consecutive backslashes. This may be a result of combining several strings to form the path and inadvertently including too many backslashes.  
  
### To correct this error  
  
-   Examine the registry key being specified to determine where and why the extra backslashes are being inserted.  
  
## See Also  
 [How to: Parse File Paths in Visual Basic](../Topic/How%20to:%20Parse%20File%20Paths%20in%20Visual%20Basic.md)   
 [My.Computer.Registry Object](../vs140/My.Computer.Registry-Object.md)