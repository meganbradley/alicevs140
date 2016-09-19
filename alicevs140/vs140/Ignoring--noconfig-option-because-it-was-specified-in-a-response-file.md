---
title: "Ignoring -noconfig option because it was specified in a response file"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
H1: Ignoring /noconfig option because it was specified in a response file
ms.assetid: 87fb393d-e17f-4e50-8d98-d9dfeba30c3e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Ignoring -noconfig option because it was specified in a response file
The `/noconfig` option tells the compiler not to compile with the Vbc.rsp file. However, the compiler processes the Vbc.rsp file before processing any other response files, so the compiler cannot honor the `/noconfig` option in a response file.  
  
 **Error ID:** BC2025  
  
### To correct this error  
  
1.  Remove the `/noconfig` option from the response file.  
  
2.  Specify the `/noconfig` option when invoking the command-line compiler.  
  
## See Also  
 [/noconfig](../vs140/-noconfig.md)   
 [@ (Specify Response File) (Visual Basic)](../vs140/@--Specify-Response-File---Visual-Basic-.md)