---
title: "-imports (Visual Basic)"
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
H1: /imports (Visual Basic)
ms.assetid: 9a93fb53-c080-497b-bf9b-441022dbbc39
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -imports (Visual Basic)
Imports namespaces from a specified assembly.  
  
## Syntax  
  
```  
/imports:namespaceList  
```  
  
## Arguments  
  
|||  
|-|-|  
|Term|Definition|  
|`namespaceList`|Required. Comma-delimited list of namespaces to be imported.|  
  
## Remarks  
 The `/imports` option imports any namespace defined within the current set of source files or from any referenced assembly.  
  
 The members in a namespace specified with `/imports` are available to all source-code files in the compilation. Use the [Imports Statement (.NET Namespace and Type)](../Topic/Imports%20Statement%20\(.NET%20Namespace%20and%20Type\).md) to use a namespace in a single source-code file.  
  
||  
|-|  
|To set /imports in the Visual Studio integrated development environment|  
|1.  Have a project selected in **Solution Explorer**. On the **Project** menu, click **Properties**. For more information, see [Introduction to the Project Designer](assetId:///898dd854-c98d-430c-ba1b-a913ce3c73d7).<br />2.  Click the **References** tab.<br />3.  Enter the namespace name in the box beside the **Add User Import** button.<br />4.  Click the **Add User Import** button.|  
  
## Example  
 The following code compiles when `/imports:system` is specified.  
  
 [!CODE [VbVbalrCompiler#21](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCompiler#21)]  
  
## See Also  
 [Visual Basic Command-Line Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)   
 [References and the Imports Statement](../vs140/References-and-the-Imports-Statement--Visual-Basic-.md)   
 [Sample Compilation Command Lines](../vs140/Sample-Compilation-Command-Lines--Visual-Basic-.md)