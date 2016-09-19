---
title: "-optimize"
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
H1: /optimize
ms.assetid: fcba4a97-3622-4b87-a891-0f77deab4998
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -optimize
Enables or disables compiler optimizations.  
  
## Syntax  
  
```  
/optimize[ + | - ]  
```  
  
## Arguments  
  
|||  
|-|-|  
|Term|Definition|  
|`+` &#124; `-`|Optional. The `/optimize-` option disables compiler optimizations. The `/optimize+` option enables optimizations. By default, optimizations are disabled.|  
  
## Remarks  
 Compiler optimizations make your output file smaller, faster, and more efficient. However, because optimizations result in code rearrangement in the output file, `/optimize+` can make debugging difficult.  
  
 All modules generated with `/target:module` for an assembly must use the same `/optimize` settings as the assembly. For more information, see [/target (Visual Basic)](../Topic/-target%20\(Visual%20Basic\).md).  
  
 You can combine the `/optimize` and `/debug` options.  
  
||  
|-|  
|To set /optimize in the Visual Studio integrated development environment|  
|1.  Have a project selected in **Solution Explorer**. On the **Project** menu, click **Properties**.<br />     For more information, see [Introduction to the Project Designer](assetId:///898dd854-c98d-430c-ba1b-a913ce3c73d7).<br />2.  Click the **Compile** tab.<br />3.  Click the **Advanced** button.<br />4.  Modify the **Enable optimizations** check box.|  
  
## Example  
 The following code compiles `T2.vb` and enables compiler optimizations.  
  
```  
vbc t2.vb /optimize  
```  
  
## See Also  
 [Visual Basic Command-Line Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)   
 [/debug (Visual Basic)](../vs140/-debug--Visual-Basic-.md)   
 [Sample Compilation Command Lines](../vs140/Sample-Compilation-Command-Lines--Visual-Basic-.md)   
 [/target (Visual Basic)](../Topic/-target%20\(Visual%20Basic\).md)