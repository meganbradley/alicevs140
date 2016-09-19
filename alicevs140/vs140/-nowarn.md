---
title: "-nowarn"
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
H1: /nowarn
ms.assetid: 7ebf2106-0652-4fdc-bf60-70fc86465d83
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -nowarn
Suppresses the compiler's ability to generate warnings.  
  
## Syntax  
  
```  
/nowarn[:numberList]  
```  
  
## Arguments  
  
|||  
|-|-|  
|Term|Definition|  
|`numberList`|Optional. Comma-delimited list of the warning ID numbers that the compiler should suppress. If the warning IDs are not specified, all warnings are suppressed.|  
  
## Remarks  
 The `/nowarn` option causes the compiler to not generate warnings. To suppress an individual warning, supply the warning ID to the `/nowarn` option following the colon. Separate multiple warning numbers with commas.  
  
 You need to specify only the numeric part of the warning identifier. For example, if you want to suppress BC42024, the warning for unused local variables, specify `/nowarn:42024`.  
  
 For more information on the warning ID numbers, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
||  
|-|  
|To set /nowarn in the Visual Studio integrated development environment|  
|1.  Have a project selected in **Solution Explorer**. On the **Project** menu, click **Properties**. For more information, see [Introduction to the Project Designer](assetId:///898dd854-c98d-430c-ba1b-a913ce3c73d7).<br />2.  Click the **Compile** tab.<br />3.  Select the **Disable all warnings** check box to disable all warnings.<br />     - or -<br />     To disable a particular warning, click **None** from the drop-down list adjacent to the warning.|  
  
## Example  
 The following code compiles `T2.vb` and does not display any warnings.  
  
```  
vbc /nowarn t2.vb  
```  
  
## Example  
 The following code compiles `T2.vb` and does not display the warnings for unused local variables (42024).  
  
```  
vbc /nowarn:42024 t2.vb  
```  
  
## See Also  
 [Visual Basic Command-Line Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)   
 [Sample Compilation Command Lines](../vs140/Sample-Compilation-Command-Lines--Visual-Basic-.md)   
 [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md)