---
title: "&#39;End&#39; statement cannot be used in class library projects"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c8606b17-b50b-4014-b76e-b748d57e9389
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;End&#39; statement cannot be used in class library projects
Class library projects used to create DLLs do not allow the use of the `End` keyword to stop the execution of code in a procedure.  
  
 **Error ID:** BC30615  
  
### To correct this error  
  
-   Use control structures such as `While` and `For` to control the flow of program execution.  
  
## See Also  
 [Control Flow](../vs140/Control-Flow-in-Visual-Basic.md)