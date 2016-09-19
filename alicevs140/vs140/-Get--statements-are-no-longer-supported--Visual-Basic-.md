---
title: "&#39;Get&#39; statements are no longer supported (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6aa62dcc-99aa-4051-a81e-3bbb6a8c355f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Get&#39; statements are no longer supported (Visual Basic)
`Get` statements are no longer supported. File I/O functionality is normally available in the `Microsoft.VisualBasic` namespace, but the targeted version of the .NET Compact Framework does not support it.  
  
 **Error ID:** BC30767  
  
### To correct this error  
  
-   Perform file operations with functions defined in the <xref:System.IO?qualifyHint=False> namespace.  
  
## See Also  
 <xref:System.IO?qualifyHint=False>   
 [Get Statement](../vs140/Get-Statement.md)   
 [File Access with Visual Basic](../vs140/File-Access-with-Visual-Basic.md)