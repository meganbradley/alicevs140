---
title: "&#39;Line&#39; statements are no longer supported (Smart Device-Visual Basic Compiler Error)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
H1: &#39;Line&#39; statements are no longer supported (Smart Device/Visual Basic Compiler Error)
ms.assetid: e7a17c77-06bb-4d33-966e-addb4f51caaf
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Line&#39; statements are no longer supported (Smart Device-Visual Basic Compiler Error)
The `Line` statement is no longer supported. File I/O functionality is normally available as <xref:Microsoft.VisualBasic.FileSystem.LineInput?qualifyHint=True>, but the targeted version of the .NET Compact Framework does not support it.  
  
 **Error ID:** BC30768  
  
### To correct this error  
  
-   If performing file access, use the functions defined in the <xref:System.IO?qualifyHint=False> namespace.  
  
-   If performing graphics, use <xref:System.Drawing.Graphics.DrawLine?qualifyHint=True>.  
  
## See Also  
 <xref:System.IO?qualifyHint=False>   
 <xref:System.Drawing?qualifyHint=False>   
 [File Access with Visual Basic](../vs140/File-Access-with-Visual-Basic.md)