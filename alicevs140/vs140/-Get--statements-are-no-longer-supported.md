---
title: "&#39;Get&#39; statements are no longer supported"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8d798357-7efb-4423-9808-8b20777b97ba
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Get&#39; statements are no longer supported
`Get` statements are no longer supported. File I/O functionality is available in the `Microsoft.VisualBasic` namespace.  
  
 `Get` is not supported for file operations, and can only be used in property procedure syntax.  
  
 **Error ID:** BC30829  
  
### To correct this error  
  
1.  Perform file operations using the members of `System.IO`, `FileSystemObject`, and [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] run-time functions.  
  
## See Also  
 [Processing Drives, Directories, and Files](../vs140/Processing-Drives--Directories--and-Files--Visual-Basic-.md)   
 [Get Statement](../vs140/Get-Statement.md)   
 [File Access with Visual Basic](../vs140/File-Access-with-Visual-Basic.md)