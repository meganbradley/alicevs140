---
title: "Keywords as Element Names in Code (Visual Basic)"
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
ms.assetid: 2e4e8e02-23f7-49b9-a1c8-2b0402b6b525
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Keywords as Element Names in Code (Visual Basic)
Any program element — such as a variable, class, or member — can have the same name as a restricted keyword. For example, you can create a variable named `Loop`. However, to refer to your version of it — which has the same name as the restricted `Loop` keyword — you must either precede it with a full qualification string or enclose it in square brackets (`[ ]`), as the following example shows.  
  
 [!CODE [VbVbcnConventions#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnConventions#8)]  
  
 If you do not do either of these, then Visual Basic assumes use of the intrinsic `Loop` keyword and produces an error, as in the following example:  
  
 `' The following statement causes a compiler error.`  
  
 `Loop.Visible = True`  
  
 You can use square brackets when referring to forms and controls, and when declaring a variable or defining a procedure with the same name as a restricted keyword. It can be easy to forget to qualify names or include square brackets, and thus introduce errors into your code and make it harder to read. For this reason, we recommend that you not use restricted keywords as the names of program elements. However, if a future version of Visual Basic defines a new keyword that conflicts with an existing form or control name, then you can use this technique when updating your code to work with the new version.  
  
> [!NOTE]
>  Your program also might include element names provided by other referenced assemblies. If these names conflict with restricted keywords, then placing square brackets around them causes Visual Basic to interpret them as your defined elements.  
  
## See Also  
 [Visual Basic Naming Conventions](../Topic/Visual%20Basic%20Naming%20Conventions.md)   
 [Program Structure and Code Conventions](../vs140/Program-Structure-and-Code-Conventions--Visual-Basic-.md)   
 [Visual Basic Keywords](../vs140/Keywords--Visual-Basic-.md)