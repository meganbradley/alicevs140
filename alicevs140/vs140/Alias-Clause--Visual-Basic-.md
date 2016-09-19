---
title: "Alias Clause (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 58c06b11-465d-4d87-906a-73200a3d7f19
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Alias Clause (Visual Basic)
Indicates that an external procedure has another name in its DLL.  
  
## Remarks  
 The `Alias` keyword can be used in this context:  
  
 [Declare Statement](../Topic/Declare%20Statement.md)  
  
 In the following example, the `Alias` keyword is used to provide the name of the function in advapi32.dll, `GetUserNameA`, that `getUserName` is used in place of in this example. Function `getUserName` is called in sub `getUser`, which displays the name of the current user.  
  
 [!CODE [VbVbalrStatements#15](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#15)]  
  
## See Also  
 [Keywords (Visual Basic)](../vs140/Keywords--Visual-Basic-.md)